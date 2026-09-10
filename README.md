# DEOResolve v3 — MVP real

Base React Native/Expo com Supabase para o DEOResolve.

## Incluído
- Login e criação de conta
- Perfil Cliente ou Profissional
- Chamados reais no Supabase
- Profissional vê chamados abertos
- Profissional pode aceitar chamado
- Atualização de status
- Realtime para mudanças de chamados
- Localização do aparelho
- Seleção de foto
- Interface mobile inspirada no modelo DEOResolve

## Configuração
1. Instale Node.js e Expo CLI.
2. Crie um projeto no Supabase.
3. No SQL Editor, execute `supabase/schema.sql`.
4. Copie `.env.example` para `.env` e preencha as duas variáveis.
5. Rode `npm install`.
6. Rode `npx expo start`.

### E-mail
Para testes rápidos, pode desativar temporariamente a confirmação de e-mail em Authentication > Providers > Email no Supabase. Em produção, mantenha confirmação de e-mail e configure seu domínio/remetente.

## Próxima camada de produção
- upload real de fotos para Supabase Storage
- mapa com rotas
- notificações push
- chat cliente/profissional
- pagamentos Pix/cartão
- verificação documental
- painel administrativo web
- antifraude e moderação
- publicação Google Play/App Store
