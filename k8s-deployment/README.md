# Kubernetes Deployment Project

This project demonstrates deploying a Dockerized Node.js app on Kubernetes.

## Includes
- Deployment (2 replicas)
- Service (NodePort)
- Containerized application

## How to Deploy
```
kubectl apply -f k8s/deployment.yml
kubectl apply -f k8s/service.yml
```
