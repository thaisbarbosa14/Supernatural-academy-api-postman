# Postman CI com GitHub Actions

Este repositório contém um workflow do GitHub Actions configurado para executar testes de API com Postman e gerar um relatório HTML usando o reporter Htmlextra.

## Passo a passo e estrutura do Arquivo YAML do Workflow

O arquivo `yml` do workflow define os seguintes passos:

1. **Checkout do Repositório**
    ```yaml
    - name: Checkout Repository
      uses: actions/checkout@v2
    ```

2. **Verificar Versões do Newman e Node**
    ```yaml
    - name: Step 1 Check version Newman and Node
      run: |
          newman --version
          node --version
    ```

3. **Instalar Newman-Reporter-HtmlExtra**
    ```yaml
    - name: Step 2 Install Newman-Reporter-HtmlExtra
      run: sudo npm install -g newman-reporter-htmlextra
    ```

4. **Executar Testes da Coleção do Postman**
    ```yaml
    - name: Step 3 Execute collection
      run: newman run ./supernatural_collection.json -e ./supernatural_environment.json -g ./supernatural_globals.json --reporters cli,htmlextra --reporter-htmlextra-browserTitle "Report API Supernatural" --reporter-htmlextra-title "Report API Supernatural" --reporter-htmlextra-export ./docs/index.html
    ```

5. **Upload do Relatório de Teste**
    ```yaml
    - name: Upload Test Report
      if: success()
      uses: actions/upload-artifact@v2
      with:
        name: test-report
        path: ./docs/index.html
    ```

## Execução do Workflow

O workflow é acionado em push para a branch `main` e em pull requests para a branch `main`.

## Próximos Passos

Após configurar o workflow do GitHub Actions, você pode monitorar a execução dos testes e o upload do relatório de teste no GitHub Actions e verificar os resultados dos testes no relatório HTML gerado no diretório `./docs/`.



