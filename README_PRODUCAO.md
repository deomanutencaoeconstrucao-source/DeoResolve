# DEOResolve — publicação na internet

## 1. Supabase
Crie um projeto no Supabase, execute `supabase/schema.sql` no SQL Editor e obtenha a URL e a chave anon/public.

Configure as variáveis de ambiente do projeto:
- `EXPO_PUBLIC_SUPABASE_URL`
- `EXPO_PUBLIC_SUPABASE_ANON_KEY`

Nunca coloque `service_role` no aplicativo.

## 2. Expo / EAS
Instale Node.js e execute:

```bash
npm install
npx expo install
npm install -g eas-cli
npx eas login
npx eas init
```

O `eas init` cria o projeto EAS e substitui o `projectId` em `app.json`.

## 3. Teste web local

```bash
npx expo start --web
```

## 4. Deploy web

```bash
npx expo export --platform web
npx eas deploy --prod
```

O EAS Hosting fornece uma URL pública `*.expo.app`. Depois é possível configurar domínio próprio.

## 5. Android

APK de teste:

```bash
eas build --platform android --profile preview
```

Produção:

```bash
eas build --platform android --profile production
```

## 6. iOS

```bash
eas build --platform ios --profile production
```

A publicação nas lojas exige contas de desenvolvedor Google Play e Apple e as credenciais de assinatura correspondentes.

## 7. CI/CD
O arquivo `.eas/workflows/deploy-web.yml` publica automaticamente a versão web quando houver push na branch `main` depois que o projeto EAS estiver conectado.

## Importante antes de anunciar ao público
O MVP ainda precisa de produção comercial para pagamentos, upload persistente de fotos, chat, push notifications, mapa/rotas, verificação documental, moderação, termos de uso, política de privacidade, antifraude e painel administrativo.
