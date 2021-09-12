# my-todo-list
Este é um gerenciador de lista de tarefas simples feito em Node.js.
<br>
Ele foi retirado do [Docker Tutorial 101](https://www.docker.com/101-tutorial).


## Rodando localmente (sem uso do Docker)
Este app pode ser executado localmente, em uma máquina Linux, ou usando a infraestrutura do Docker.

Como pré-requisito, você precisa ter:
[Node.js](http://nodejs.org/), o [NPM](https://www.npmjs.com/) e o [Yarn](https://yarnpkg.com/) instalados.
<br><br>
Para quem for usar o Termux, instale com o comando abaixo.
```sh 
$ pkg install nodejs
```

Para quem usa Ubuntu (ou WSL/Ubuntu no Windows), use os comandos abaixo.
```sh 
$ sudo apt update
$ sudo apt install nodejs
$ sudo apt install npm
$ npm install --global yarn
```
<br>
Agora execute.

```sh
$ node --version # verificar versão do node
$ npm --version # verificar versão do NPM
$ git --version # verificar versão do GIT
$ yarn --version # verificar versão do Yarn
$ git clone https://github.com/<SEU-USUARIO>/my-todo-list.git #fazer clone do projeto (no seu fork)
$ cd my-todo-list
$ npm install
$ yarn install --production
$ npm start
```

Pronto. Abra o navegador e digite [http://localhost:3000/](http://localhost:3000/).

----

## Rodando localmente em conteiner (com uso do Docker)
Junto com a aplicação, está disponível um Dockerfile com os seguintes comandos.

```Docker
FROM node:12-alpine
RUN apk add --no-cache python g++ make
WORKDIR /app
COPY . .
RUN yarn install --production
CMD ["node", "src/index.js"]
```

Crie a imagem do contêiner usando o comando docker build.
```sh
$ docker build -t my-todo-list .
```

A flag -t cria um legível para a imagem final, então podemos usar este nome para nos referir a esta imagem quando executamos um contêiner.
<br>
Agora que temos uma imagem, vamos executar o app! Para fazer isso, usaremos o comando docker run
1. ```$ docker run -dp 3000:3000 getting-started```

As flags -d significa executar o contêiner em mode _deatached_ ou em background (sem iteração com terminal) e a flag -p cria um mapeamento entre a porta 3000 do host e a porta 3000 do contêiner.

2. Após alguns segundos, abra seu navegador em [http://localhost:3000](http://localhost:3000). Você deve ver o app em execução!

3. Vá em frente e adicione um ou dois itens e veja se funciona conforme o esperado. Você pode marcar itens como completos e remover itens. Seu front-end está armazenando itens no back-end com sucesso!
