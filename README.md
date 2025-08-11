# Task 5 - Kubernetes with Minikube

## Objective
Deploy and manage an application in Kubernetes using Minikube inside WSL.

## Steps Performed
1. Started Minikube with Docker driver.
2. Built and pushed custom image: `netrika0210/task5-nginx:latest`.
3. Created `deployment.yaml` and `service.yaml`.
4. Deployed to Kubernetes and verified pods/services.
5. Scaled replicas from 2 to 4.
6. Checked logs and pod details.

## Commands
```bash
minikube start --driver=docker
docker build -t netrika0210/task5-nginx:latest .
docker push netrika0210/task5-nginx:latest
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
kubectl scale deployment task5-deployment --replicas=4
kubectl describe pod <pod-name>
kubectl logs <pod-name>
