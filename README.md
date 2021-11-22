# Simple React

Exemplo de aplicativo React.js para o ambiente Docker desenvolvida em uma máquina Ubuntu.

## Prerequisites

Certifique-se de já ter instalado o Docker Engine. Você não precisa instalar o Nginx (caso for usar desse servidor) ou o NPM, pois ambos são fornecidos pelas imagens do Docker.

```
$ docker -v
Docker version 20.10.7, build 20.10.7-0ubuntu5~20.04.2
```
```
$ docker-compose -v
docker-compose version 1.29.2, build 5becea4c
```

## Path

Primeiramente precisamos criar nosso projeto React.js
```
$ npx create-react-app .
```
teste
```
$ npm start
```
Após criar o arquivo Dockerfile, execute o comando para criar sua imagem
```
$ docker build -t react-image .
```
Esse comando, cria um contêiner "react-app" a partir da imagem "react-image" 
```
$ docker run -d —name react-app react-image
```
Enterrompa seu contêiner para a criação do arquivo docker-compose.yml
```
$ docker stop react-app
```
e então execute-o para a rodar a partir do arquivo criado
```
$ docker-compose up -d
```

## Installing

Para executar o atual repositório em sua máquina (de preferência usar uma 
distribuição Ubuntu/Debian) run os seguintes comandos:
```
git clone https://github.com/jeffalves33/reactJS-Docker.git
cd reactJS-Docker
docker build -t react-image .
docker run -d —name react-app react-image
```


## Built With

* [Node](https://nodejs.org/en/) - back-end
* [React.js](https://reactjs.org/) - The front-end framework used
* [Docker](https://www.docker.com/) - Containerization
* [Express](https://expressjs.com/) - back-end requests


## Authors

* **Jeferson Alves** - *Trabalho Inicial* - [jeffalves33](https://github.com/jeffalves33)

## Upcoming Updates

* Tratar de como o Docker faz permanecer o servidor no ar;
* mudar servidor para Nginx;
* rotas;








