# Análise A/B 

## Este é um código em Python executado em um ambiente Jupyter Notebook em um contêiner Docker. O código está usando as bibliotecas numpy e pandas para manipulação de dados.

## INSTRUÇÕES 

**Instação do docker e criação do container**

- Passo 1: Instalar o Docker

- Passo 2: Executar o dockerfile 
    - OBS: Essas instruções irão criar uma imagem de container baseada na imagem oficial do Python 3.8, instalar o VS Code e o Jupyter, configurar o VS Code para usar o Jupyter e expor a porta 8888 para o acesso ao Jupyter Notebook.

- Passo 3: No terminal, navegue até o diretório onde você criou o arquivo Dockerfile e execute 
o seguinte comando para construir a imagem do container:
    - *docker build -t vscode-jupyer .*
    O ponto (.) no final do comando indica que o Docker deve usar o diretório atual como contexto para construir a imagem.

- Passo 4: Executar o container 
    - docker run -p 8888:8888 vscode-jupyer
    


