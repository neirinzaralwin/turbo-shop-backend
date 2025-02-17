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

## Project Structure

