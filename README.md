# Kubernetes Nginx Deployment Demo

This project demonstrates how to deploy a simple *Nginx web server* using *Kubernetes* on *Minikube* (running locally using Docker on Windows 11).

## Prerequisites

- [Minikube](https://minikube.sigs.k8s.io/docs/start/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)
- [Git](https://git-scm.com/)
- Docker Desktop

## Project Structure
kubernetes-demo/ ├── deployment.yaml   # Defines Nginx Deployment └── service.yaml      # Exposes Nginx Deployment as NodePort service

## Steps Performed
1. *Started Minikube*  
   bash(terminal)
   minikube start
2. Created deployment
   kubectl apply -f deployment.yaml
3. Created service
   kubectl apply -f service.yaml
4. Verified pod and service status
   kubectl get pods
   kubectl get services
5. Scaled deployment to 4 replicas
   kubectl scale deployment
   nginx-deployment --replicas=4
7. Accessed application in browser
   minikube service nginx-service

Output
Nginx pods are running.  http://127.0.0.1:61782
Nginx service accessible via NodePort.
Verified Nginx server running in browser.
