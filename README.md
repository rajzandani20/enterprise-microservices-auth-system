
# 🚀 **Enterprise Microservices Authentication System (Phase 1–8)**

### *Production-Ready | Spring Boot | JWT (RSA) | API Gateway | OTP | RBAC | Docker | Microservices Architecture*

This repository contains a **complete 8-phase enterprise microservices project**, including:

* Authentication Service (RSA-based JWT, Refresh Tokens, OTP)
* User Service (RBAC, Admin Panel APIs)
* API Gateway (Routing + Rate Limiting + JWT Filter)
* Discovery Service (Eureka)
* Config Server (Centralized Config Management)
* Logs Service (Activity Logging)
* Docker Compose (Full Microservices Orchestration)
* Swagger Documentation
* Postman API Collection
* Global Exception Handling + Validation
* Unit Tests

---

# 📌 **📘 Table of Contents**

* [Architecture Overview](#architecture-overview)
* [Microservices Included](#microservices-included)
* [Technology Stack](#technology-stack)
* [Phase Breakdown](#phase-breakdown)
* [How to Run](#how-to-run)
* [API Documentation](#api-documentation)
* [Postman Collection](#postman-collection)
* [Screenshots](#screenshots)
* [Project Folder Structure](#project-folder-structure)
* [Future Enhancements](#future-enhancements)
* [License](#license)

---

# 🏗 **Architecture Overview**

```
                   ┌───────────────────────┐
                   │     Client (Postman)   │
                   └─────────────┬─────────┘
                                 │
                        (JWT, RBAC, Rate Limit)
                                 │
                  ┌──────────────▼──────────────┐
                  │      API Gateway (8080)      │
                  └──────────────┬──────────────┘
                                 │
       ┌───────────────┬────────┴────────┬───────────────┐
       │               │                 │                │
┌────────────┐  ┌──────────────┐  ┌────────────┐  ┌─────────────────┐
│Auth-Service│  │User-Service  │  │Logs-Service│  │Config-Service    │
│   (9001)   │  │   (9002)     │  │   (9003)   │  │     (8888)       │
└────────────┘  └──────────────┘  └────────────┘  └─────────────────┘
                                 │
                          ┌──────────────┐
                          │Discovery     │
                          │Service (8761)│
                          └──────────────┘
```

---

# 🔥 **Microservices Included**

### ✔ **1. Auth-Service (9001)**

* RSA JWT Access/Refresh Tokens
* Token Rotation + Revocation
* OTP-based Password Reset
* Login, Register APIs
* Global Exception Handling
* Password Validation

---

### ✔ **2. User-Service (9002)**

* RBAC (Admin/User)
* Admin endpoints
* User profile fetch/update

---

### ✔ **3. Gateway-Service (8080)**

* Routing to all microservices
* JWT Validation
* Redis-based Rate Limiting

---

### ✔ **4. Discovery-Service (8761)**

* Eureka Server
* Microservice registry
* Dashboard UI

---

### ✔ **5. Config-Service (8888)**

* Centralized configuration
* Profile-based config management

---

### ✔ **6. Logs-Service (9003)**

* Login logs
* OTP request logs
* Admin logs

---

# 🧰 **Technology Stack**

| Layer         | Technology                   |
| ------------- | ---------------------------- |
| Backend       | Spring Boot 3, Spring MVC    |
| Auth          | JWT (RSA256), Refresh Tokens |
| Security      | Spring Security              |
| Microservices | Spring Cloud Netflix         |
| Registry      | Eureka                       |
| Gateway       | Spring Cloud Gateway         |
| Config        | Spring Cloud Config          |
| Logs          | Centralized Log Service      |
| DB            | PostgreSQL                   |
| Cache         | Redis                        |
| Build         | Maven                        |
| Deployment    | Docker + Docker Compose      |
| Testing       | JUnit, Mockito               |

---

# 📦 **Phase Breakdown (1–8 Completed)**

### **Phase 1 – Skeleton**

Microservices basic structure + Docker Compose.

### **Phase 2 – Authentication Service**

JWT RSA, login, register, refresh tokens, hashing, validations.

### **Phase 3 – OTP Password Reset**

Send OTP, validate OTP, reset password API.

### **Phase 4 – User Service + RBAC**

Admin routes, role-based authorization.

### **Phase 5 – Gateway Rate Limiting**

Redis-based limiting, JWT filters.

### **Phase 6 – Activity Logs**

Login attempts, OTP usage, admin events.

### **Phase 7 – Infrastructure**

Eureka, Config Server, full microservice bootstrap.

### **Phase 8 – Final Build**

Docker Compose finalization, Swagger, Postman, diagrams, README.

---

# ▶️ **How to Run**

### **1. Clone the repo**

```bash
git clone https://github.com/YOUR_USERNAME/enterprise-microservices-auth-system.git
cd enterprise-microservices-auth-system
```

### **2. Start Docker Services**

```bash
docker compose up --build
```

### **3. Access Services**

| Service              | URL                                                                            |
| -------------------- | ------------------------------------------------------------------------------ |
| API Gateway          | [http://localhost:8080](http://localhost:8080)                                 |
| Eureka Dashboard     | [http://localhost:8761](http://localhost:8761)                                 |
| Config Server        | [http://localhost:8888](http://localhost:8888)                                 |
| Auth-Service Swagger | [http://localhost:9001/swagger-ui.html](http://localhost:9001/swagger-ui.html) |
| User-Service Swagger | [http://localhost:9002/swagger-ui.html](http://localhost:9002/swagger-ui.html) |

---

# 📘 **API Documentation (Swagger)**

Each microservice exposes Swagger:

```
http://localhost:9001/swagger-ui.html
http://localhost:9002/swagger-ui.html
http://localhost:9003/swagger-ui.html
```

---

# 🔥 **Postman Collection**

Located inside:

```
/postman-collection/
```

Includes:

* Login
* Register
* Refresh
* OTP
* Admin APIs
* Logs

---



# 📁 **Project Folder Structure**

```
phase-1-skeleton/
phase-2-auth-service/
phase-3-otp-password/
phase-4-user-rbac/
phase-5-gateway-rate-limit/
phase-6-logs-service/
phase-7-infra/
phase-8-final-build/
```

---

# 🚀 **Future Enhancements**

* Kubernetes Deployment
* CI/CD Pipeline via GitHub Actions
* Distributed Tracing (Zipkin)
* ELK Logging

---


# What’s New

This project introduces a full enterprise-grade microservices architecture with independent Auth, User, Gateway, Config, Discovery, and Logs services.
It adds advanced security features like RSA-signed JWTs, refresh token rotation, OTP password reset, RBAC, centralized configs, Eureka discovery, and Redis rate limiting.
The entire system is production-ready, fully containerized with Docker Compose, complete with Swagger docs, Postman APIs, activity logging, and a scalable cloud-ready structure.

---

# 📜 **License**

```
MIT License
```

---

