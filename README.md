# NLW

## Executando a Aplicação Ecoleta 

Para executar este projeto será preciso instalar inicialmente o Node e o React.

Para instalar as dependências do projeto usa-se o comando 'npm install x' onde x serão os pacotes. Também há outras dependências 
no mobile que precisarão ser instaladas usando 'expo install x'.

Para executar cada stack use os seguintes comandos.

Em [/server](https://github.com/edjust/NLW/tree/master/server):

Dependências que precisarão ser instaladas: 

npm install x = [express, typescript, ts-node, ts-node-dev, knex, sqlite3, cors, multer, celebrate]

* ```npm run knex:migrate``` para criar o banco de dados da aplicação;
* ```npm run knex:seed``` para inserir os itens ao banco de dados;
* ```npm run dev``` para executar o server da aplicação.

Com o servidor executado, o endereço utilizado para ver se está funcionando é [http://localhost:3333/items](http://localhost:3333/items). 
É importante acessar os arquivos do [src/controllers](https://github.com/edjust/NLW/tree/master/server/src/controllers) e verificar 
os IPs externos estáticos definidos. Eles foram usados para acessar arquivos a partir da aplicação mobile.

![](https://github.com/edjust/NLW/blob/master/images/print/serverRunning.png)

Em [/web](https://github.com/edjust/NLW/tree/master/web):

Dependências que precisarão ser instaladas: 

npm install x = [react-icons, react-router-dom, leaflet, react-leaflet, axios, react-dropzone]

* ```npm start``` para executar a aplicação web.

Será aberta uma aba do seu navegador com o endereço [http://localhost:3000/](http://localhost:3000/) com a aplicação. 
Aqui é feito o cadastro de pontos de coleta. Todos os dados devem ser preenchidos para realizar o cadastro.

![](https://github.com/edjust/NLW/blob/master/images/print/webCadastro2.png)

Em [/mobile](https://github.com/edjust/NLW/tree/master/mobile):

Dependências que precisarão ser instaladas: 

npm install x = [expo-cli, @react-navigation/native, @react-navigation/stack, axios]

expo install x = [expo-font @expo-google-fonts/ubuntu @expo-google-fonts/roboto, react-native-gesture-handler react-native-reanimated react-native-screens react-native-safe-area-context @react-native-community/masked-view, 
react-native-maps, react-native-svg, expo-location, expo-mail-composer]

* ```npm start``` para executar a aplicação mobile.

Será aberta uma aba do seu navegador com o endereço [http://localhost:19002/](http://localhost:19002/) abrindo o Expo Metro Bundler. 
Com ela pode ser feita a simulação da aplicação a partir de um simulador de dispositivo instalado na sua máquina ou pode ser aberto num 
dispositivo físico usando o QR Code mostrado. Obs.: Tem que ser baixado no dispositivo físico o App Expo, e dispositivo e PC tem que estar 
na mesma rede usando a conexão LAN do Metro Bundler.

![](https://github.com/edjust/NLW/blob/master/images/print/metroBundler.png)

## Principais tecnologias da Aplicação Ecoleta

Aplicação de cadastro e visualização de pontos de coleta de lixo, o Ecoleta. Foi criada uma API RESTful que retorna os dados do nosso Back-end (Node.js) de uma forma estruturada para que o Front-end Web (ReactJS) e Front-end Mobile (React Native) consigam interpretar e mostrar o conteúdo em tela. 

TypeScript auxiliou bastante no desenvolvimento e facilitou na visualização de informações como o formato de parâmetros e métodos de bibliotecas. A biblioteca Knex (Query Builder) permite trabalhar com bancos de dados SQL construindo as query em formato JS. Com ela tem-se a vantagem de poder continuar utilizando apenas JavaScript, podendo tirar vantagem da IntelliSense da IDE, neste projeto foi usado VSCode. Ela também pode ser adaptada para qualquer bando de dados. Então, utilizando o formato do Knex, se futuramente precisar mudar por exemplo de Postgre pro Oracle, vai continuar funcionando da mesma forma. 

ReactJS mostrou ser uma biblioteca com bastante praticidade, principalmente para criar interfaces, e com grandes funcionalidades. Uma delas é poder escrever HTML diretamente dentro do JavaScript. Para integrar um mapa na aplicação web usou-se o uma biblioteca de mapa open source, o Leaflet, onde o React possui outra biblioteca que permite integrá-la ao projeto. O Front-end se comunicou com o Back-end utilizando a biblioteca Axios que faz requisições à API, obtendo os recursos precisos para mostrar em tela. Ela também foi utilizada para  obter recursos da API de localidade do IBGE, um serviço de dados que por exemplo nesta aplicação foi utilizada a de Estados e Cidades. É nessa aplicação web que é feita os cadastros de pontos de coleta.

Para finalizar o projeto, foi desenvolvido uma aplicação mobile usando a framework React Native. Ela mostra como funciona o desenvolvimento de linguagem multiplataforma, permitindo o App estar disponível para diversas plataformas mobile, a partir de um código comum. Para simular o app utilizou-se o Expo, que permite o acesso às API’s nativas do dispositivo sem precisar instalar qualquer dependência ou alterar código nativo. O mesmo pode ser usado num dispositivo físico baixando o app pela loja de aplicativos ou pelo simulador da IDE Android ou XCode. Para aplicações simples é uma ferramenta boa, mas para projetos com maior complexidade pode haver conflitos. Foram usados aplicativos externos como o do mapa nativo para a busca de pontos da API e envio de mensagens a partir do redirecionamento para o aplicativo de E-mail nativo e What’s App. Nesta aplicação é feita a busca dos pontos de coleta a partir do estado, cidade e dos itens selecionados, como também é possível entrar em contato via What’s App e E-mail do ponto.


