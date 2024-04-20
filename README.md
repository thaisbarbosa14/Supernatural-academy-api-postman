# Postman CI com GitHub Actions

Este repositório contém um workflow de CI para rodar testes do Postman usando GitHub Actions.

## Descrição do Workflow

O workflow é configurado para ser acionado em push para as branches `main` em pull requests para estas branches. O workflow é executado em um ambiente `ubuntu-latest` e usa as seguintes etapas:

### 1. Checkout Repository

Faz checkout do repositório para o ambiente de execução.

### 2. Install Node.js

Instala o Node.js versão 16 para atender ao requisito mínimo de versão do Newman.

### 3. Install Newman

Instala o Newman, um executor de coleções Postman.

### 4. Run Postman Tests

Executa os testes do Postman usando os arquivos `supernatural_collection.json`, `supernatural_environment.json` e `supernatural_globals.json` e gera um relatório HTML em `./docs/index.html`.

#### Comando Newman

```bash
newman run ./supernatural_collection.json \
  -e ./supernatural_environment.json \
  -g ./supernatural_globals.json \
  --reporters cli,htmlextra \
  --reporter-htmlextra-browserTitle "Report Supernatural" \
  --reporter-htmlextra-title "Report Supernatural" \
  --reporter-htmlextra-export ./docs/index.html


