# TinyURL Microservices

A scalable, containerized **URL Shortener** application built with **Java (Spring Boot)**, **Redis**, and deployed using **Docker**, **Kubernetes (Minikube)**, and **Helm** — powered by **GitHub Actions CI/CD**.

---

## ✨ Features

- **Microservice Architecture**: Separate services for shortening and resolving URLs
- **Spring Boot** with Gradle for clean, testable Java code
- **Redis** as a lightning-fast in-memory store
- **CI/CD** pipeline with GitHub Actions (build, test, Dockerize, push)
- **Kubernetes Deployment** via Helm Charts
- **Local Dev & Test** using Docker Compose or Minikube

---

## 📁 Project Structure

```bash
TinyUrl/
├── .github/
│   └── workflows/
│       └── cicd.yaml          # GitHub Actions pipeline
├── tinyurl/                   # Helm chart (templates, values)
├── url-shortener/            # Spring Boot service to shorten URLs
│   └── Dockerfile
├── url-resolver/             # Spring Boot service to resolve shortened URLs
│   └── Dockerfile
└── README.md
```
---

## ⚙️ Technologies Used
- **Java 17 + Spring Boot**
- **Redis**
- **Docker & Docker Compose**
- **Kubernetes (Minikube)**
- **Helm**
- **GitHub Actions (CI/CD)**

## 🚀 Setup Instructions
- **Clone the Repo**
- **cd TinyUrl**
- **Build and Run with Docker Compose (Local Dev) -> docker-compose up --build**
- **Minikube + Helm (Local K8s Deployment)**
    - **minikube start**
    - **helm install tinyurl .**

## ✅ GitHub Actions CI/CD
- **Trigger: Every push to main branch**
- **Actions Performed:**
    - **Build both Spring Boot apps**
    - **Run tests**
    - **Build and push Docker images to Docker Hub**
    - **Secrets required in GitHub:**
        - **DOCKER_USERNAME**
        - **DOCKER_PASSWORD**

---
## 🧪 API Endpoints (Sample)
```bash
POST /api/shorten
{
  "longUrl": "https://example.com"
}
```
Resolve a Short URL
```bash
GET /{shortId}
```
---
## 🛡 Future Enhancements
- **Push to real Kubernetes cluster (GKE, EKS)**
- **Ingress + HTTPS via cert-manager**

## 🤝 Contributing
- **Feel free to fork this repo, create feature branches, and submit PRs!**
  
## License
- **MIT License - © 2026 Debashis Satapathy**
