# Análise de anúncios

## Este é um código em Python executado em um ambiente Jupyter Notebook em um contêiner Docker. O código está usando as bibliotecas numpy e pandas para manipulação de dados.

# Sobre o dataset 
| Coluna | Descrição|
| ---| --- |
| auction_id | o identificador único do usuário online que foi apresentado ao questionário BIO. Em terminologia padrão, isso é chamado de ID de impressão. O usuário pode ver o questionário BIO, mas optar por não responder. Nesse caso, as colunas "yes" e "no" são ambas zero 
| experiment | a qual grupo o usuário pertence - controle ou exposto|
| control | usuários que viram um anúncio fictício|
| exposed | usuários que viram um anúncio criativo, um anúncio online interativo, com a marca SmartAd|
| date | a data no formato AAAA-MM-DD|
| hour | a hora do dia no formato HH|
| device_make | o nome do tipo de dispositivo que o usuário possui, por exemplo, Samsung|
| platform_os | o ID do sistema operacional que o usuário possui|
| browser | o nome do navegador que o usuário utiliza para visualizar o questionário BIO|
| yes | 1 se o usuário escolher o botão de rádio "Sim" para o questionário BIO|
| no | 1 se o usuário escolher o botão de rádio "Não" para o questionário BIO|

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
    
# Conclusão

Com base na análise, o anúncio interativo online com a **marca SmartAd** foi considerado *mais eficaz do que* o **anúncio fictício** na geração de *engajamento do usuário e cliques*. **A taxa de cliques para o grupo exposto foi de 0,0769, que é maior** do que a taxa de cliques para o grupo de **controle de 0,0648**. *A diferença entre os dois grupos é de 0,0120*, indicando que o *anúncio interativo online foi mais eficaz na geração de engajamento do usuário.*

As *principais marcas de dispositivos* com as maiores taxas de cliques para o grupo exposto foram **VFD 700, A0001, VCE-L22, HTC Desire 2, e OnePlus ONEPLUS A3000**. Os *principais navegadores com as maiores taxas de cliques para o grupo exposto **foram Chrome, Chrome Mobile WebView, Chrome Mobile, Facebook, e Samsung Internet**. 

Esses resultados sugerem que o anúncio interativo online com **a marca SmartAd pode ser mais eficaz para determinados tipos de dispositivos e navegadores, e que direcionar esses tipos específicos de dispositivos e navegadores pode resultar em taxas de engajamento mais altas.**

