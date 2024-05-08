# DESCRIÇÃO:
Projeto desenvolvido pela equipe Supernatural como parte do treinamento oferecido pela Qa.Coders Academy, com o objetivo de aprimorar as habilidades práticas em automação de testes de API, com integração contínua (CI) com o GitHub Actions para realizar testes automatizados com Postman e Newman. Este README fornece informações sobre as tecnologias utilizadas, como instalá-las, como configurar o ambiente e como executar os testes.


## Tecnologias Utilizadas

- [Postman](https://www.postman.com/)
- [Newman](https://github.com/postmanlabs/newman)
- Node.js
- GitHub Actions
  
## Como Instalar as Tecnologias

1. **Postman**
    - Baixe o Postman no [site oficial](https://www.postman.com/downloads/).
    - Siga as instruções de instalação para o seu sistema operacional.

2. **Node.js**
    - Baixe o instalador do [site oficial](https://nodejs.org/).
    - Execute o instalador e siga as instruções de instalação.

3. **Newman**
    - Abra um terminal após instalar o Node.js.
    - Execute o comando `npm install -g newman` para instalar Newman globalmente.

4. **Newman Reporter HTML Extra**
    - Para instalar o módulo `newman-reporter-htmlextra`, execute o comando:
        ```shell
      npm install -g newman-reporter-htmlextra
      ```

## Como Instalar o Ambiente

1. Clone este repositório para o seu ambiente local:
    ```shell
    git clone [URL do repositório]
    ```

2. Navegue até a pasta do projeto:
    ```shell
    cd [nome_da_pasta_do_projeto]
    ```

3. Verifique se Node.js e Newman estão instalados corretamente seguindo as instruções acima.

## Como Rodar os Testes no Postman

1. Abra o Postman.
2. Importe a coleção de testes do projeto.
3. Configure o ambiente necessário a partir dos arquivos de ambiente do projeto.
4. Execute os testes na coleção usando o botão "Run" dentro da interface gráfica do Postman.

## Como Rodar os Testes no Newman

1. No terminal, navegue até a pasta do projeto:
    ```shell
    cd [nome_da_pasta_do_projeto]
    ```

2. Execute a coleção de testes com Newman especificando a coleção e o ambiente:

    ```shell
    newman run [caminho_para_a_colecao] -e [caminho_para_o_ambiente] --reporters cli,htmlextra --reporter-htmlextra-export [caminho_para_o_relatorio]
    ```

    Exemplo:

    ```shell
    newman run Supernatural/Departament-New/Adicionar-Departamento.postman_collection.json -e Supernatural/Departament-New/Supernatural.postman_environment.json --reporters cli,htmlextra --reporter-htmlextra-export Supernatural/Departament-New/docs/index.html
    ```
   

## Projeto Desenvolvido por:
| [<img loading="lazy" src="https://avatars.githubusercontent.com/u/32967494" width=90><br/><sub>Carine Gehlen</sub>](https://github.com/cgehlen)<br/>[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/carinegehlen/)](https://www.linkedin.com/in/carinegehlen/) | [<img loading="lazy" src="https://avatars.githubusercontent.com/u/119118485" width=90><br/><sub>Damião Silva</sub>](https://github.com/damiaojsilva2)<br/>[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/damiaojsilva/)](https://www.linkedin.com/in/damiaojsilva/) | [<img loading="lazy" src="https://avatars.githubusercontent.com/u/157240964" width=90><br/><sub>Florencio Santos Junior</sub>](https://github.com/fasjunior2204)<br/>[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/florencio-santos-junior/)](https://www.linkedin.com/in/florencio-santos-junior/) | [<img loading="lazy" src="https://avatars.githubusercontent.com/u/118402799" width=90><br/><sub>Marcial Genari</sub>](https://github.com/Genari22)<br/>[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/marcial-genari-477a7824b/)](https://www.linkedin.com/in/marcial-genari-477a7824b/) |
| :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| [<img loading="lazy" src="https://avatars.githubusercontent.com/u/57133248" width=90><br/><sub>Noele Guimarães</sub>](https://github.com/noeleguimaraes)<br/>[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/noeleguimaraes/)](https://www.linkedin.com/in/noeleguimaraes/) | [<img loading="lazy" src="https://avatars.githubusercontent.com/u/148631954" width=90><br/><sub>Patricia Castro Vitoriano</sub>](https://github.com/PatriciaVitoriano)<br/>[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/patricia-castro-vitoriano/)](https://www.linkedin.com/in/patricia-castro-vitoriano/) | [<img loading="lazy" src="https://avatars.githubusercontent.com/u/82854418" width=90><br/><sub>Thaís Almeida</sub>](https://github.com/thaisbarbosa14)<br/>[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/thais-almeida-464b91180/)](https://www.linkedin.com/in/thais-almeida-464b91180/) | [<img loading="lazy" src="https://avatars.githubusercontent.com/u/116967975" width=90><br/><sub>Thaís Marchetti Contó</sub>](https://github.com/thaisconto)<br/>[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/thaismarchetticonto/)](https://www.linkedin.com/in/thaismarchetticonto/) | 
| [<img loading="lazy" src="https://avatars.githubusercontent.com/u/56051094" width=90><br/><sub>Tiago Mata</sub>](https://github.com/TiagoMata)<br/>[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/tiagosmata/)](https://www.linkedin.com/in/tiagosmata/) |

