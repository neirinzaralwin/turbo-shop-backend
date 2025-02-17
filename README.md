# TurboShop API – High-Performance GraphQL Backend

A high-performance e-commerce backend using Fastify, GraphQL, PostgreSQL, and Redis.

## Why This Project?
- Ultra-fast API using Fastify
- GraphQL for flexible queries
- PostgreSQL for reliable data storage
- Redis for caching and speed optimization
- GraphQL Subscriptions for real-time updates

---

## Features
### Authentication & Users
- JWT-based authentication
- Role-based access (Admin, Seller, Buyer)

### Product & Order Management
- Create, update, delete products
- Manage orders, update order status
- Cache frequently accessed products using Redis

### Performance Optimization
- Redis Caching for frequently requested data
- GraphQL Subscriptions for real-time order updates
- Prisma ORM for optimized PostgreSQL queries

---

## Tech Stack
| Component         | Technology |
|------------------|------------|
| Framework        | Fastify |
| API             | GraphQL (Apollo Server) |
| Database        | PostgreSQL (Prisma ORM) |
| Caching         | Redis |
| Authentication  | JWT (JSON Web Tokens) |
| Real-Time Updates | GraphQL Subscriptions (WebSockets) |

---

## Project Structure (Modular Monolith)
- Scalable architecture for microservice.
- Event driven approach
  
```bash
/turbo-shop-api
│── src/
│   ├── api/
│   │   ├── index.ts       # Fastify Server
│   │   ├── graphql/
│   │   │   ├── schema.ts  # GraphQL Schema
│   │   │   ├── resolvers.ts  # GraphQL Resolvers
│   │   ├── middleware/
│   │   │   ├── auth.ts  # JWT Authentication Middleware
│   │   ├── config/
│   │   │   ├── env.ts  # Environment Variables Loader
│   │   ├── utils/
│   │   │   ├── logger.ts  # Logger Utility
│
│   ├── modules/  # Each module acts as a future microservice
│   │   ├── users/
│   │   │   ├── user.model.ts   # Prisma User Model
│   │   │   ├── user.service.ts  # Business Logic
│   │   │   ├── user.resolver.ts # GraphQL Resolver
│   │   │   ├── user.events.ts  # Event Handlers
│   │   │   ├── user.routes.ts  # REST API (if needed)
│   │   ├── products/
│   │   │   ├── product.model.ts
│   │   │   ├── product.service.ts
│   │   │   ├── product.resolver.ts
│   │   │   ├── product.events.ts
│   │   │   ├── product.routes.ts
│   │   ├── orders/
│   │   │   ├── order.model.ts
│   │   │   ├── order.service.ts
│   │   │   ├── order.resolver.ts
│   │   │   ├── order.events.ts
│   │   │   ├── order.routes.ts
│
│   ├── db/
│   │   ├── prisma.ts   # PostgreSQL ORM Configuration
│   │   ├── redis.ts    # Redis Configuration
│
│   ├── events/
│   │   ├── eventBus.ts   # Redis Pub/Sub for Event-Driven Communication
│
│── .env                   # Environment Variables
│── package.json           # Dependencies
│── tsconfig.json          # TypeScript Config

```

