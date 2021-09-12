# my-todo-list
App para gerência tarefas 

## Rodando localmente 
Este é um gerenciador de lista de tarefas simples feito em Node.js.
Ele foi retirado do [Docker Tutorial 101](https://www.docker.com/101-tutorial).

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
