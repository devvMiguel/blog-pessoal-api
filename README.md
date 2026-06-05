# 📰 Blog Pessoal - API REST

Este projeto é uma API REST desenvolvida com **NestJS**, com foco em autenticação segura, cadastro de usuários, gerenciamento de postagens, temas e controle de permissões. Ideal para servir como back-end de um blog pessoal.

---

## 🚀 Link do Deploy (Render)

🔗 Acesse a API online através do link:  
👉 [https://blog-pessoal-mmxr.onrender.com](https://blog-pessoal-mmxr.onrender.com)

---

## ⚙️ Tecnologias Utilizadas

- NestJS
- TypeScript
- Node.js
- TypeORM
- MySQL / PostgreSQL / SQLite
- JWT (Autenticação)
- Passport.js
- Class-validator
- ESLint / Prettier
- Jest / Supertest
- Swagger (instalado)
- Dotenv (variáveis de ambiente)
- Render (deploy)

---

## 🐳 Como Executar Localmente (com Docker)

A aplicação está conteinerizada, o que significa que você não precisa instalar o MySQL ou o Node.js localmente na sua máquina para rodar o projeto. O Docker cuidará de todo o ambiente de forma automática.

### 1. Clone o repositório

```bash
git clone [https://github.com/devvMiguel/blog-pessoal.git](https://github.com/devvMiguel/blog-pessoal.git)
cd blog-pessoal
```

### 2. Configure o ambiente para Desenvolvimento

Antes de subir os containers, certifique-se de que a aplicação está configurada para olhar para o banco de dados local. 
No arquivo `src/app.module.ts`, confirme que o `TypeOrmModule` está utilizando o `DevService`:

```typescript
TypeOrmModule.forRootAsync({
  useClass: DevService,
  imports: [ConfigModule],
}),
```

### 3. Inicie a aplicação com Docker Compose

Construa a imagem e suba os containers do banco de dados e da API em segundo plano:

```bash
docker compose up -d --build
```
> **Nota:** A flag `--build` garante que o Docker leia as alterações mais recentes feitas no seu código, como a configuração do `DevService` acima.

### 4. Acesse a API

Quando os containers estiverem rodando, a API estará disponível em:  
📍 `http://localhost:4000`

---

### 🛑 Como parar a aplicação

Para derrubar os containers quando terminar de usar, basta rodar no terminal na raiz do projeto:

```bash
docker compose down
```

---

## 🛠️ Como Executar Localmente com MySQL

### 1. Clone o repositório

```bash
git clone https://github.com/devvMiguel/blog-pessoal.git
cd blog-pessoal
```

### 2. Instale as dependências

```bash
npm install
```

### 3. Configure o banco de dados MySQL

Crie um banco de dados MySQL local chamado `blog_pessoal` ou outro nome de sua escolha.

### OBS: Para rodar local altere para DevService no app.module.

### 4. Inicie o servidor

```bash
npm run start:dev
```

A API estará disponível em:  
📍 `http://localhost:4000`

---

## 🧪 Testes

Execute os testes unitários e de integração:

```bash
npm run test
```

---

## 📁 Estrutura do Projeto

```
src/
├── auth/              # Autenticação (JWT, Passport, Guards)
├── usuario/           # CRUD de usuários
├── postagem/          # CRUD de postagens
├── tema/              # CRUD de temas
├── data/              # Configuração de conexão com DB
├── main.ts            # Arquivo principal
└── app.module.ts      # Módulo raiz
```

---

## ✅ Funcionalidades

- Cadastro e login de usuário com JWT
- CRUD de temas e postagens
- Proteção de rotas com autenticação
- Relacionamentos entre entidades
- Boas práticas com validações e tratamento de erros
- Testes automatizados com Jest

---

## 📦 Deploy

Este projeto está hospedado no **Render** e pode ser facilmente adaptado para Vercel, Railway ou Heroku.

---

## ✍️ Autor

Desenvolvido por **Miguel**  
🔗 GitHub: [@devvMiguel](https://github.com/devvMiguel)

🔗 LinkedIn: [Miguel Ferreira](www.linkedin.com/in/ferreir4miguel)

## License

Nest is [MIT licensed](https://github.com/nestjs/nest/blob/master/LICENSE).

<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="120" alt="Nest Logo" /></a>
</p>

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest

  <p align="center">A progressive <a href="http://nodejs.org" target="_blank">Node.js</a> framework for building efficient and scalable server-side applications.</p>
    <p align="center">
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/v/@nestjs/core.svg" alt="NPM Version" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/l/@nestjs/core.svg" alt="Package License" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/dm/@nestjs/common.svg" alt="NPM Downloads" /></a>
<a href="https://circleci.com/gh/nestjs/nest" target="_blank"><img src="https://img.shields.io/circleci/build/github/nestjs/nest/master" alt="CircleCI" /></a>
<a href="https://discord.gg/G7Qnnhy" target="_blank"><img src="https://img.shields.io/badge/discord-online-brightgreen.svg" alt="Discord"/></a>
<a href="https://opencollective.com/nest#backer" target="_blank"><img src="https://opencollective.com/nest/backers/badge.svg" alt="Backers on Open Collective" /></a>
<a href="https://opencollective.com/nest#sponsor" target="_blank"><img src="https://opencollective.com/nest/sponsors/badge.svg" alt="Sponsors on Open Collective" /></a>
  <a href="https://paypal.me/kamilmysliwiec" target="_blank"><img src="https://img.shields.io/badge/Donate-PayPal-ff3f59.svg" alt="Donate us"/></a>
    <a href="https://opencollective.com/nest#sponsor"  target="_blank"><img src="https://img.shields.io/badge/Support%20us-Open%20Collective-41B883.svg" alt="Support us"></a>
  <a href="https://twitter.com/nestframework" target="_blank"><img src="https://img.shields.io/twitter/follow/nestframework.svg?style=social&label=Follow" alt="Follow us on Twitter"></a>
</p>
  <!--[![Backers on Open Collective](https://opencollective.com/nest/backers/badge.svg)](https://opencollective.com/nest#backer)
  [![Sponsors on Open Collective](https://opencollective.com/nest/sponsors/badge.svg)](https://opencollective.com/nest#sponsor)-->
