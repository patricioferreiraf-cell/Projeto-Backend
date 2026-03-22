# Projeto Backend

API backend desenvolvida com Node.js, Express e Sequelize, utilizando PostgreSQL via Supabase como banco de dados.

---

## 🚀 Descrição

Este projeto consiste em uma API REST para gerenciamento de produtos, categorias e suas relações. Ele permite criar, listar e manipular dados armazenados em um banco PostgreSQL na nuvem.

---

## 🛠️ Tecnologias utilizadas

* Node.js
* Express
* Sequelize
* PostgreSQL (Supabase)
* dotenv
* Nodemon

---

## ⚙️ Como rodar o projeto

### 1. Clone o repositório

```bash
git clone URL_DO_SEU_REPOSITORIO
```

### 2. Acesse a pasta do projeto

```bash
cd project-root
```

### 3. Instale as dependências

```bash
npm install
```

---

## ⚠️ Configuração do Supabase (IMPORTANTE)

Para que a conexão com o banco funcione corretamente, é necessário utilizar o **Transaction Pooler** no Supabase.

### Passos:

1. Acesse o painel do Supabase

2. Vá em: **Settings → Database**

3. Em **Connection string**, altere o método para:

   **Transaction Pooler**

4. Copie a connection string e utilize os dados no `.env`

### ⚠️ Atenção:

* A porta deve ser:

  ```
  6543
  ```

* O usuário NÃO será apenas `postgres`, será algo como:

  ```
  postgres.seu_id_do_projeto
  ```

---

## 🔐 Configuração do ambiente

Crie um arquivo `.env` na raiz do projeto:

```env
PORT=3001

DB_HOST=SEU_HOST_POOLER
DB_USER=SEU_USER_SUPABASE
DB_PASSWORD=SUA_SENHA
DB_NAME=postgres
DB_PORT=6543
DB_DIALECT=postgres

JWT_SECRET=sua_chave
JWT_EXPIRES_IN=1d
```

---

## ▶️ Rodando o projeto

```bash
npm run dev
```

O servidor estará disponível em:

```
http://localhost:3001
```

---

## 🌐 Rotas da API

### Produtos

* **GET /products**

  * Lista todos os produtos

* **POST /products**

  * Cria um novo produto

#### Exemplo de requisição:

```json
{
  "nome": "Notebook",
  "preco": 3500,
  "stock": 10,
  "description": "Notebook gamer",
  "enabled": true
}
```

---

## 🗂️ Estrutura do projeto

```
src/
 ├── models/
 ├── database/
 ├── routes/
 ├── controllers/
 └── server.js
```

---

## 🧠 Funcionalidades

* Conexão com banco PostgreSQL via Supabase
* Criação e listagem de produtos
* Estrutura preparada para expansão (categorias, opções, etc.)

---

## 👨‍💻 Autores

Atividade desenvolvida como parte avaliativa do curso de desenvolvimento Full Stack do programa Geração Tech. Realizado em dupla por Islane Costa e Patrício Felício.
