# Oficina Fácil + Mecânico Perto — edição comercial

Este pacote é a base de produção do aplicativo. Ele funciona em modo demonstração imediatamente e pode ser ligado ao Supabase para contas reais e dados online.

## 1. Banco online
1. Crie um projeto no Supabase.
2. Abra SQL Editor e execute `supabase/schema.sql`.
3. Copie a URL e a chave `anon` do projeto.
4. Edite `config.js`:
   - `SUPABASE_URL: '...'`
   - `SUPABASE_ANON_KEY: '...'`
   - `DEMO_MODE: false`

## 2. Publicação
Pode ser hospedado como site/PWA em Vercel, Netlify, Cloudflare Pages ou servidor próprio. A pasta é estática; não precisa de Node para a primeira publicação.

## 3. Recursos já estruturados
- autenticação de oficina/motorista;
- perfis e permissões por usuário (RLS);
- clientes e veículos;
- orçamentos;
- agendamentos;
- cadastro público de oficinas;
- avaliações;
- integração de contato via WhatsApp;
- PWA instalável;
- base para planos pagos.

## 4. Próximas integrações de produção
- Mercado Pago para assinatura Premium;
- geolocalização + mapa real;
- push notifications;
- upload de fotos/documentos;
- painel administrativo;
- publicação Google Play/App Store;
- termos, privacidade, LGPD e política de cancelamento;
- domínio e e-mail transacional.

Nunca coloque chaves secretas do servidor no navegador. A chave `anon` do Supabase é própria para o cliente quando RLS está configurado corretamente.
