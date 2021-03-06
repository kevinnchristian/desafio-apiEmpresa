# Desenvolver API usando MongoDB e Mongoose

### Dependências
- Instalar Express.js: `yarn add express`
- Instalar módulo CORS: `yarn add cors`
- Instalar Nodemon: `yarn add nodemon -D`
- Instalar Mongoose: `yarn add mongoose`
- Instalar .env: `yarn add dotenv`
- Instalar File System: `yarn add fs`
- Instalar Multer: `yarn add multer`
- Instalar Multer-S3: `yarn add multer-s3`
- Instalar AWS-SDK: `yarn add aws-sdk`

### Comandos utilizados:
- Para iniciar projeto node: `yarn init -y`
- Para rodar a aplicação em ambiente de desenvolvimento `yarn dev`, este comando irá executar o script: `nodemon ./src/bin/www`
- Para rodar a aplicação em produção `yarn start`, este comando irá executar o script: `node ./src/bin/www`

### Banco de Dados - MongoDB Atlas
- Criar um cluster na plataforma web `MongoDB Atlas`
- Criar um `database`
- Para conectar com banco basta criar um arquivo `.env` na raiz do projeto e inserir a `URI` que a plaforma oferece para conexão
- Rodar a aplicação para criar os documentos no banco de dados

### Software para teste:
- `Insomnia` - Testando métodos HTTP e Parâmetros
- O arquivo de testes é o `teste_insomnia_backend`, basta baixar e rodar no insomnia

### Hospedagem:
- Plataforma utilizada para hospedagem: `Heroku`
- Url principal da API: `https://api-empresa.herokuapp.com/companies`


- Rotas empresas de forma geral:
  - Listar: `https://api-empresa.herokuapp.com/companies`
  - Criar: `https://api-empresa.herokuapp.com/companies`
  - Atualizar: `https://api-empresa.herokuapp.com/companies/:company_id`
  - Deletar: `https://api-empresa.herokuapp.com/companies/:company_id`


- Rotas unidades:
  - Listar: `https://api-empresa.herokuapp.com/companies/unit/:unit_id`
  - Criar: `https://api-empresa.herokuapp.com/companies/:company_id/unit`
  - Atualizar: `https://api-empresa.herokuapp.com/companies/unit/:unit_id`
  - Deletar: `https://api-empresa.herokuapp.com/companies/:company_id/unit/:unit_id`
 
  
- Rotas ativos:
  - Listar: `https://api-empresa.herokuapp.com/companies/unit/active/:active_id`
  - Criar: `https://api-empresa.herokuapp.com/companies/unit/:unit_id/active`
  - Atualizar: `https://api-empresa.herokuapp.com/companies/active/:active_id`
  - Deletar: `https://api-empresa.herokuapp.com/companies/unit/:unit_id/active/:active_id`
 
  
- Rotas usuários:
  - Listar: `https://api-empresa.herokuapp.com/companies/user/:user_id`
  - Criar: `https://api-empresa.herokuapp.com/companies/:company_id/user`
  - Atualizar: `https://api-empresa.herokuapp.com/user/:user_id`
  - Deletar: `https://api-empresa.herokuapp.com/companies/:company_id/user/:user_id`


### Observações:
- Server está rodando na porta `3335`
- O módulo `cors` faz com que a aplicação saiba que nenhuma outra fora a nossa está tentando fazer conexão com a nossa API
- O arquivo `.env.example` tem o exemplo de como deve ser criado o arquivo `.env`, este arquivo tem que conter a URI que o `Mongo Atlas` disponibiliza para conexão com banco
- `Multer` é o middleware express utilizado manipular requisições multipart-form, são requisições que traz arquivos
- `Multer-S3` nos permite configurar storage na `AWS`
- `AWS-SDK` é uma lib que contém todas as configurações da AWS, com a integração Node.js com a API da AWS(neste caso seria API do S3)
