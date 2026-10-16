# 📘 Booking Platform — Cloud-Native Reference Implementation

A modern, end‑to‑end booking platform built with **React**, **.NET**, **Azure**, **Infrastructure‑as‑Code**, and **Azure DevOps pipelines**.  
This project demonstrates clean architecture, service boundaries, cloud deployment patterns, and enterprise‑grade engineering practices.

It is designed as a **7‑day build plan**, showcasing rapid delivery while maintaining architectural clarity and production‑ready patterns.

---

## 🚀 Tech Stack

### **Frontend**
- React (Vite)
- React Router
- React Query
- TypeScript

### **Backend**
- .NET 8 Minimal APIs
- Background Worker (Queue processing)
- Domain‑driven structure
- Shared contracts + messaging abstractions

### **Infrastructure**
- Azure App Service / Azure Container Apps
- Azure Service Bus
- Azure Cosmos DB / Azure SQL
- Azure Storage
- Bicep modules
- Terraform modules

### **DevOps**
- Azure DevOps YAML pipelines
- Multi‑stage CI/CD (dev → qa → uat → prod)
- Pipeline templates
- Environment definitions
- Variable groups + service connections

---

## 📁 Folder Structure

```
booking-platform/
│
├── backend/
│   ├── events-service/
│   │   ├── src/                 # Core API code (controllers, services, domain)
│   │   ├── tests/               # Unit + integration tests
│   │   └── README.md            # Service-specific documentation
│   │
│   ├── booking-service/
│   │   ├── src/                 # Core API code
│   │   ├── worker/              # Background worker (queues, schedulers)
│   │   ├── tests/               # Unit + integration tests
│   │   └── README.md
│   │
│   └── shared/
│       ├── contracts/           # Shared DTOs, message contracts
│       ├── messaging/           # Service Bus/Kafka abstractions
│       └── README.md
│
├── frontend/
│   └── react-app/
│       ├── src/                 # React components, hooks, pages
│       ├── public/              # Static assets
│       └── README.md
│
├── infrastructure/
│   ├── azure/
│   │   ├── bicep/               # Bicep IaC modules
│   │   ├── terraform/           # Terraform IaC modules
│   │   └── pipelines/           # Azure DevOps YAML pipelines
│   │
│   └── azure-devops/
│       ├── templates/           # Reusable pipeline templates
│       ├── environments/        # Dev/QA/UAT/Prod environment definitions
│       └── docs/                # DevOps setup + pipeline documentation
│
├── docs/
│   ├── architecture.md          # System architecture overview
│   ├── sequence-diagrams.md     # Flow diagrams
│   ├── deployment.md            # Deployment strategy
│   ├── observability.md         # Logging, metrics, tracing
│   └── decisions/               # Architecture Decision Records (ADRs)
│
└── README.md                    # Project overview + quickstart
```

---

## 🧭 7‑Day Build Plan (High-Level)

### **Day 1 — Frontend Setup**
- React app
- Routing
- Basic pages
- Initial UI scaffolding

### **Day 2 — Backend Setup**
- .NET minimal API
- Health checks
- Basic endpoints

### **Day 3 — Domain + Messaging**
- Shared contracts
- Messaging abstractions
- Event flow design

### **Day 4 — Infrastructure**
- Bicep modules
- Terraform modules
- Resource group + core services

### **Day 5 — CI/CD**
- Azure DevOps pipelines
- Templates
- Multi‑stage YAML

### **Day 6 — Environments**
- dev / qa / uat / prod YAMLs
- Variable groups
- Service connections

### **Day 7 — Documentation**
- Architecture.md
- ADRs
- Sequence diagrams
- Deployment strategy

---

## ▶️ Running the Project

### **Frontend**
```
cd frontend/react-app
npm install
npm run dev
```

### **Backend**
```
cd backend/events-service/src
dotnet run
```

```
cd backend/booking-service/src
dotnet run
```

### **Worker**
```
cd backend/booking-service/worker
dotnet run
```

---

## ☁️ Deployment

Deployment is handled through **Azure DevOps multi‑stage pipelines**:

- Build → Test → Publish → Deploy  
- Infrastructure deployment via Bicep/Terraform  
- Application deployment via Azure DevOps environments  
- Approvals for QA/UAT/Prod  

See:

```
infrastructure/azure/pipelines/
infrastructure/azure-devops/templates/
infrastructure/azure-devops/environments/
```

---

## 📚 Documentation

All architecture and engineering documentation lives under:

```
docs/
```

Key files:

- `architecture.md` — system design  
- `sequence-diagrams.md` — request flows  
- `deployment.md` — CI/CD + infra  
- `observability.md` — logs, metrics, tracing  
- `decisions/` — ADRs  

---

## 🏁 Status

This project is actively being built.
