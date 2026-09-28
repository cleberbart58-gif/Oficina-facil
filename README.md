# Oficina Fácil — pacote Android pronto para GitHub Actions

Este ZIP contém o aplicativo web/PWA e toda a configuração necessária para o GitHub Actions criar o projeto Android e gerar um arquivo AAB.

## Como gerar o AAB

1. Envie **todos os arquivos e pastas deste ZIP** para a raiz do repositório GitHub `cleberbart58-gif/Oficina-facil`.
2. Abra **Actions**.
3. Selecione **Build Android AAB**.
4. Toque em **Run workflow** e confirme na branch `main`.
5. Quando terminar, abra a execução concluída e baixe o artefato **oficina-facil-aab**.

O workflow instala as dependências, cria automaticamente a pasta `android/`, sincroniza `www/` e gera `app-debug.aab`. Portanto, a pasta `android/` não precisa estar dentro deste ZIP.

## O que foi conferido

- `package.json` válido.
- Capacitor 8 configurado.
- Node 22 configurado no GitHub Actions.
- Java 21 configurado no GitHub Actions.
- `npx cap add android` configurado.
- `npx cap sync android` configurado.
- Geração de AAB com `bundleDebug` configurada.
- Verificação automática de que o AAB realmente existe antes do upload.
- Arquivos JavaScript sem erro de sintaxe detectável.
- `manifest.json` e `package.json` válidos.
- Arquivos HTML principais presentes.

## Importante sobre o AAB

O arquivo gerado é um **AAB de debug**, adequado para validar o aplicativo e o processo de build. Para publicar na Google Play, ainda será necessário configurar a assinatura de produção e os dados da publicação.

## Configuração do aplicativo

O identificador Android é `br.com.oficinafacil.app` e o nome do aplicativo é **Oficina Fácil**.

A interface web fica em `www/`.

## Dados online

O aplicativo abre em modo demonstração por padrão. A integração real com Supabase depende da configuração do banco e das políticas RLS.

Os campos de configuração ficam em `www/config.js`:

- `SUPABASE_URL`
- `SUPABASE_ANON_KEY`
- `DEMO_MODE`

Nunca coloque chaves secretas de servidor no navegador.
