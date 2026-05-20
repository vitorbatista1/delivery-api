# Delivery API

API REST para gerenciamento de pedidos de delivery construída com arquitetura escalável, autenticação JWT, cache distribuído, documentação automática e ambiente totalmente containerizado.

---

## Objetivo

Fornecer uma API robusta para operações de delivery contendo:

- Autenticação e autorização
- Gestão de usuários
- Restaurantes
- Produtos
- Carrinho
- Pedidos
- Pagamentos
- Cache
- Documentação
- Testes automatizados

---

## Stack

### Backend

- Node.js
- TypeScript
- NestJS

### Banco de dados

- PostgreSQL

### Infraestrutura

- Docker
- Redis

### Qualidade

- Swagger (OpenAPI)
- Jest
- ESLint
- Husky
- Commitlint

---

## Arquitetura

```txt
src/

modules/
├── auth
├── users
├── restaurants
├── products
├── cart
├── orders
└── payments

shared/
├── database
├── cache
├── auth
└── config

common/
├── guards
├── interceptors
├── filters
└── decorators
```

---

## Funcionalidades

### Autenticação

- Cadastro
- Login
- JWT
- Refresh Token

### Usuários

- Criar conta
- Atualizar perfil
- Buscar usuário

### Restaurantes

- Cadastro
- Listagem
- Atualização

### Produtos

- CRUD completo
- Controle de estoque

### Carrinho

- Adicionar itens
- Remover itens

### Pedidos

- Criar pedido
- Atualizar status
- Histórico

### Pagamentos

- Simulação de pagamento
- Webhook

---

## Tecnologias

| Tecnologia | Função |
|---|---|
| NestJS | Framework |
| PostgreSQL | Persistência |
| Redis | Cache |
| Docker | Containers |
| Prisma | ORM |
| Swagger | Documentação |

---

## Ambiente local

### Clonar

```bash
git clone <repo>
```

```bash
cd delivery-api
```

---

## Variáveis

Crie:

`.env`

```env
PORT=3000

DATABASE_URL=postgresql://admin:admin@postgres:5432/delivery

REDIS_HOST=redis

REDIS_PORT=6379

JWT_SECRET=secret
```

---

## Executar

Subir containers:

```bash
docker compose up -d
```

Instalar:

```bash
npm install
```

Executar migrations:

```bash
npx prisma migrate dev
```

Rodar:

```bash
npm run start:dev
```

---

## Documentação

Swagger:

```txt
http://localhost:3000/docs
```

---

## Testes

Unitários:

```bash
npm run test
```

Cobertura:

```bash
npm run test:cov
```

E2E:

```bash
npm run test:e2e
```

---

## Estrutura Git

Branches:

```txt
main
develop
feature/*
fix/*
```

Padrão de commit:

```txt
feat:
fix:
refactor:
docs:
test:
chore:
```

Exemplo:

```bash
git commit -m "feat(order): create order endpoint"
```

---

## Roadmap

- [ ] Auth JWT
- [ ] Usuários
- [ ] Restaurantes
- [ ] Produtos
- [ ] Carrinho
- [ ] Pedidos
- [ ] Pagamentos
- [ ] Redis
- [ ] Testes E2E
- [ ] CI/CD

---

## Autor

Desenvolvido por Vitor Batista.