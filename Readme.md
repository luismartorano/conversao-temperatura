# Iniciativa Kubernetes - Aula 1 - Desafio: App node


### Dockerfile criado - imagem Node 14
O arquivo Dockerfile deve estar na raiz da aplicação, no nosso caso é "src".

```
FROM node:14

WORKDIR /usr/src/app

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 8080
CMD [ "node", "server.js" ]

```

### Imagem personalizada
```
docker image build . -t luismartorano/conversaotemperatura:2.0

```
### Executando o container docker na porta 49160
```
docker container run -p 49160:8080 -d luismartorano/conversaotemperatura:1.0
```

### Verificando processo
```
docker container ps

```
### Executando programa
```
localhost:49160

```
### Destruindo o container

```
docker container rm -f <nome do container>

```