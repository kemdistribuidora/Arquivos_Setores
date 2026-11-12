# Painel de Planilhas por Setor — Distribuidora KEM

Painel que lista as planilhas do Google Sheets de cada setor.

- **Front-end:** `index.html`, publicado no GitHub Pages: https://kemdistribuidora.github.io/Arquivos_Setores/
- **Back-end:** `api/Code.gs` (fica só local, fora do git), que roda no Google Apps Script. Os dados ficam na aba `Dados` da planilha configurada em `SPREADSHEET_ID`.

## Atualizar o back-end

1. Cole o conteúdo de `api/Code.gs` no editor do Apps Script e salve com Ctrl+S.
2. Vá em **Implantar → Gerenciar implantações**, clique no lápis, escolha **Nova versão** e clique em **Implantar**.
   Assim a URL `/exec` continua a mesma. Se você criar uma **Nova implantação**, a URL muda e é preciso atualizar `URL_APPS_SCRIPT` no `index.html`.

## Senha de administrador

A senha mestre, que remove qualquer planilha, não fica no código.
Para defini-la, abra no Apps Script **Configurações do projeto → Propriedades do script** e adicione a propriedade `SENHA_ADMIN`.
Sem essa propriedade, cada planilha só pode ser removida com a própria senha.
