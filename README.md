# ☸️ Kubernetes Deployment for Dockerized Application

This project demonstrates how to deploy a containerized Node.js application on a **Kubernetes Cluster**.  
It includes Deployment, Service, and Docker configuration to simulate real cloud-native environments.

---

## 📌 Project Overview

The app is containerized using Docker, then deployed to Kubernetes using:

- **Deployment** (2 replicas for high availability)
- **Service (NodePort)** – to expose the application
- Optional: Ingress (can be added for routing)

This setup reflects a real-world microservices deployment workflow.

---

## 🧱 Tech Stack

- **Node.js** – Sample application  
- **Docker** – Container runtime  
- **Kubernetes (K8s)** – Orchestration  
- **kubectl** – Cluster management  

---

## 📂 Project Structure

```
k8s-deployment/
│
├── app/
│   ├── app.js
│   ├── package.json
│   └── Dockerfile
│
└── k8s/
    ├── deployment.yml
    └── service.yml
```

---

## 🚀 How to Deploy

### 1️⃣ Build Docker Image
```
docker build -t amrosw/app:latest .
```

### 2️⃣ Apply Deployment
```
kubectl apply -f k8s/deployment.yml
```

### 3️⃣ Apply Service
```
kubectl apply -f k8s/service.yml
```

### 4️⃣ Verify Pods
```
kubectl get pods
```

### 5️⃣ Access Application
```
kubectl get service devops-service
```

---

## 📝 Notes

This project demonstrates a **real Kubernetes production pattern**:

- Multiple replicas  
- Container image pulled from registry  
- NodePort access  
- Modular YAML configuration  

It can be extended with:

- Ingress Controller  
- Horizontal Pod Autoscaling  
- Resource limits  
- ConfigMaps & Secrets  

---



Created by Amro Housam Aldeen
