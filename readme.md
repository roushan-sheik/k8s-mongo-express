# Kubernetes Demo Project

This project demonstrates how to deploy MongoDB and Mongo Express in a Kubernetes cluster using Minikube.

## 🚀 Deployment (Apply Commands in Order)

Execute the following commands in sequence to create the necessary resources:

```bash
kubectl apply -f mongo-secret.yaml
kubectl apply -f mongo.yaml
kubectl apply -f mongo-configmap.yaml 
kubectl apply -f mongo-express.yaml
```

## 🔍 Inspection & Monitoring Commands

Use these commands to view the status of your cluster resources:

```bash
kubectl get pod
kubectl get pod --watch
kubectl get pod -o wide
kubectl get service
kubectl get secret
kubectl get all | grep mongodb
```

## 🐛 Debugging Commands

If something goes wrong, you can inspect the resources and view logs:

```bash
# Replace 'xxxxxx' with the actual pod name suffix
kubectl describe pod mongodb-deployment-xxxxxx
kubectl describe service mongodb-service
kubectl logs mongo-express-xxxxxx
```

## 🌐 Accessing the Application

To get a direct URL to the external service running in Minikube, run:

```bash
minikube service mongo-express-service
```