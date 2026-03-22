# GoCart E-Commerce Platform

GoCart is a full-stack, multi-vendor e-commerce project with a microservices backend and a Next.js frontend.

This repository is organized as a mono-repo so contributors and reviewers can understand the complete system in one place.

## What this project includes

- Microservices backend built with Java, Spring Boot, and Spring Cloud
- API Gateway for unified entry and routing
- Frontend storefront and admin/store pages built with Next.js
- Docker support for local multi-service runs
- CI/CD and Azure deployment guidance

## High-level architecture

The backend is split into independent services, each with a focused responsibility:

- Gateway (entry point and routing)
- User Service (authentication, user profiles, addresses)
- Store Service (store management)
- Product Service (catalog and ratings)
- Order Service (checkout/order lifecycle)
- Notification Service (notifications and messaging workflows)

The frontend consumes backend APIs through the gateway.

## Repository structure

```text
e-com/
├── backend/                  # Spring Boot microservices and gateway
│   ├── gateway/
│   ├── user-service/
│   ├── store-service/
│   ├── product-service/
│   ├── order-service/
│   ├── notification-service/
│   └── docker-compose.yml
├── frontend/                 # Next.js application
└── DEPLOYMENT_AZURE.md       # Azure deployment and CI/CD notes
```

## Quick start

### Option 1: Run backend with Docker Compose (recommended)

```bash
cd backend
docker-compose up --build
```

### Option 2: Run frontend locally

```bash
cd frontend
npm install
npm run dev
```

Frontend default URL:

- http://localhost:3000

## Documentation

- Backend details: `backend/README.md`
- Frontend details: `frontend/README.md`
- Azure deployment guide: `DEPLOYMENT_AZURE.md`

## Tech stack

- Backend: Java 17, Spring Boot, Spring Security, OpenFeign, Maven
- Frontend: Next.js, React, Tailwind CSS, Redux Toolkit
- Containers: Docker, Docker Compose
- Deployment target: Azure Container Apps (documented)

## Notes

This repository appears to be prepared for academic cloud-computing coursework and demo workflows, while also being structured like a production-style e-commerce system.
