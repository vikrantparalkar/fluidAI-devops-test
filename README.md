# DevOps Engineer Infrastructure Challenge

Production-style Kubernetes deployment with CI/CD, GitOps, Helm templating, PostgreSQL persistence, and operational debugging.

---

# Project Overview

This project demonstrates a complete DevOps workflow for deploying a Python REST API application on Kubernetes using modern CI/CD and GitOps practices.

The system includes:

- Python REST API with CRUD operations
- PostgreSQL database integration
- Docker containerization
- Kubernetes deployment on Minikube
- Helm templating
- GitHub Actions CI pipeline
- ArgoCD continuous deployment
- Persistent Volume handling
- Failure simulation and debugging

---

# Architecture

```text
Developer Pushes Code
        │
        ▼
GitHub Actions CI Pipeline
 ├── Install Dependencies
 ├── Run Lint Checks
 ├── Run Tests
 ├── Build Docker Image
 ├── Push Docker Image to Docker Hub
 └── Update Helm values.yaml image tag
        │
        ▼
Git Repository Updated
        │
        ▼
ArgoCD Detects Git Change
        │
        ▼
Automatic Kubernetes Deployment
        │
        ▼
Minikube Kubernetes Cluster
 ├── Python REST API
 ├── PostgreSQL Database
 ├── Persistent Volume Claims
 └── Kubernetes Services
