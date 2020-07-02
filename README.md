# NLW

## Aplicação Ecoleta

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
