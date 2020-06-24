<h1 align="center">
  Challenge GoStack Transactions 🚀
  <p align="center">
  <img src="https://img.shields.io/badge/tech-backend-lightgrey" />

  <a href="https://nodejs.org/en/">
    <img src="https://img.shields.io/badge/framework-NodeJS-green" />
  </a>
  
  <a href="https://www.typescriptlang.org/">
    <img src="https://img.shields.io/badge/framework-typescript-blue" />
  </a>
  
   <a href="https://www.postgresql.org/">
    <img src="https://img.shields.io/badge/database-postgreSQL-green" />
  </a>
  
  <a href="https://typeorm.io/#/">
    <img src="https://img.shields.io/badge/framework-typeORM-red" />
  </a>

  <a href="https://insomnia.rest/">
    <img src="https://img.shields.io/badge/tests-insomnia-blueviolet" />
  </a>
  
  <a href="https://github.com/Rocketseat">
    <img src="https://img.shields.io/badge/source-rocketseat-blueviolet" />
  </a>
  </p>
</h1>

## 🔖 Sobre o desafio 

Segundo desafio em [NodeJS](https://nodejs.org/en/ "NodeJS") usando [TypeScript](https://www.typescriptlang.org/ "TypeScript") da [RocketSeat](https://rocketseat.com.br/ "RocketSeat"), passado no bootcamp GoStack 12. 

O desafio proposto foi desenvolver uma aplicação de gestão de transações, incluindo o uso de banco de dados [PostgreSQL](https://www.postgresql.org/ "PostgreSQL") com o [TypeORM](https://typeorm.io/#/ "TypeORM") e envio de arquivos com o [Multer](https://www.npmjs.com/package/multer "Multer")!

Essa será uma aplicação que deve armazenar transações financeiras de entrada e saída e permitir o cadastro e a listagem dessas transações, além de permitir a criação de novos registros no banco de dados a partir do envio de um arquivo csv.

## 💻 Tecnologias 

- <img width="20px" src="https://img.icons8.com/color/2x/nodejs.png" /> [NodeJS](https://nodejs.org/en/ "NodeJS")
- <img width="20px" src="https://img.icons8.com/color/2x/typescript.png" /> [TypeScript](https://www.typescriptlang.org/ "TypeScript")
- <img width="20px" src="https://res.cloudinary.com/practicaldev/image/fetch/s--00h6CjGb--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://www.maxrooted.com/panduan-membangun-rest-api-expressjs-mysql/cover.png" /> [Express](https://expressjs.com/ "Express")
- <img width="20px" src="https://img.icons8.com/color/2x/postgreesql.png" /> [PostgreSQL](https://www.postgresql.org/ "PostgreSQL")
- <img width="20px" src="https://avatars2.githubusercontent.com/u/20165699?s=400&v=4" /> [TypeORM](https://typeorm.io/#/ "TypeORM") - Framework para queries
- <img width="20px" src="https://img.icons8.com/dusk/2x/dbeaver.png" />  [Dbeaver](https://dbeaver.io/download/ "Dbeaver") - Gerenciador de banco de dados
- <img width="20px" src="https://insomnia.rest/images/icon-small.png" /> [Insomnia](https://insomnia.rest/ "Insomnia") - Efetuando testes das requisições

## ▶️ Getting Started 
- **Passo** 1️⃣ : Executar a instalação do [NodeJS](https://nodejs.org/en/ "NodeJS") e [Docker](https://www.docker.com/ "Docker")
- **Passo** 2️⃣ : Git clone do projeto [gostack-transacions-typeorm](https://github.com/rafaelsanzio/gostack-transactions-typeorm "gostack-transacions-typeorm")
- **Passo** 3️⃣ : Acessar a pasta do projeto e executar os seguintes comandos 👇🏽
```bash
  # Navegando até a pasta do projeto
  $ cd gostack-transactions-typeorm

  # Criando uma visão no Docker para criação do Banco de Dados
  $ docker run --name <nome-da-visao> -e POSTGRES_PASSWORD=<password> -p <porta:porta> -d postgres
```
- **Passo** 4️⃣ : Criar banco de dados no seu administrador (Ex: [Dbeaver](https://dbeaver.io/download/ "Dbeaver"))
- **Passo** 5️⃣ : Alterar o arquivo **ormconfig.json** para suas configurações do banco de dados (username, password, database)

- **Passo** 7️⃣ : Ainda na pasta do projeto execute os seguintes comandos 👇🏽
```bash
  # Instalando todas as depêndencias necessárias
  $ yarn install

  # Realizando migrações para criar tabelas no banco de dados
  $ yarn typeorm migration:run

  # Starting o backend da aplicação
  $ yarn dev:server
```

## 🛠 Casos de Teste
```json
/* Requisição de criação de transação */
🟢 POST - /transactions
params: {
  "title": "Depósito Nubank",
  "value": 3000,
  "type": "income",
  "category": "Salary"
}

/* Requisições de listagens de transações */
🟣 GET - /transactions 

/* Requisição de exclusão de transação */
🔴 DELETE - /transactions/{id}

/* Requisição de importação de CSV - transações */
🟢 POST - /transactions/import
params: {
  "file": "import-template.csv",
}

/* Layout CSV - title type value category */

```
## :congratulations: Considerações 
- Projeto desenvolvido no Bootcamp - GoStack da [RocketSeat](https://rocketseat.com.br/ "RocketSeat")  by:

- <img width="20px" src="https://img.icons8.com/fluent/96/github.png" /> [Rafael Sanzio](https://github.com/rafaelsanzio "Rafael Sanzio")
 
- <img width="20px" src="https://img.icons8.com/color/2x/linkedin.png" /> [Rafael Sanzio](https://www.linkedin.com/in/rafael-sanzio-012778143/ "Rafael Sanzio")
