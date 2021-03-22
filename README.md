### start test  ###
npm run test
npm run test-comportamento

### start app ###
npm start

### build ###
npm install

-------------------------------------------
### Gerar o build do docker ###
docker build -t didox/validador-cpf-nodejs-turma-devops -f Dockerfile .

### Rodar imagem docker e gravar localmente ###
docker run -d -p 3000:3000 --name validador-cpf-nodejs-turma-devops didox/validador-cpf-nodejs-turma-devops
### Rodar imagem docker em modo iterativo localmente ###
docker run -it -p 3000:3000 --name validador-cpf-nodejs-turma-devops didox/validador-cpf-nodejs-turma-devops

### Para parar o seriviço rodar ###
docker stop validador-cpf-nodejs-turma-devops

### Para startar o seriviço rodar ###
docker start validador-cpf-nodejs-turma-devops

### Para remover o seriviço rodar ###
docker rm validador-cpf-nodejs-turma-devops

### Para fazer login no dockerhub ###
docker login

### Criar a tag apontando para o repositório do docker hub ###
docker tag didox/validador-cpf-nodejs-turma-devops hub.docker.com/r/didox/validador-cpf-nodejs-turma-devops

### Fazer o push da imagem para a docker hub ###
docker push didox/validador-cpf-nodejs-turma-devops
-------------------------------------------