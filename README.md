# Capstone Application Repository

This repository contains the containerized web application and CI/CD pipeline.

## Application Stack
- **Frontend**: Static HTML/CSS website
- **Container**: Nginx Alpine
- **Orchestration**: Kubernetes (K3s)
- **CI/CD**: GitHub Actions

## Local Development
```bash
docker build -t capstone-app .
docker run -p 8080:80 capstone-app
```

## Kubernetes Deployment
```bash
kubectl apply -f k8s/
kubectl get pods
kubectl get svc
```

## CI/CD Pipeline
- Triggers on push to main branch
- Builds Docker image
- Pushes to Docker Hub
- Deploys to Kubernetes cluster

## Access
- Local: http://localhost:8080
- Production: http://[MASTER_IP]:30080