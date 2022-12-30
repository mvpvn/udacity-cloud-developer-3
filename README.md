# Udagram Image Filtering Application

## Getting started 

### Prerequisite
1. Environment

`kubectl apply -f aws-secret.yaml`

`kubectl apply -f env-secret.yaml`

`kubectl apply -f env-configmap.yaml`

2. Network

`sh aws/create-network.sh`

### 1. Database

`sh aws/create-rds.sh`

### 2. S3

`sh aws/create-s3.sh`

### 3. EKS

`sh aws/create-eks.sh`

### 4. Backend API

`kubectl apply -f k8s/backend-feed-deployment.yaml`

`kubectl apply -f k8s/backend-feed-service.yaml`

`kubectl apply -f k8s/backend-user-deployment.yaml`

`kubectl apply -f k8s/backend-user-service.yaml`

### 4. Reverse proxy

`kubectl apply -f k8s/reverseproxy-deployment.yaml`

`kubectl apply -f k8s/reverseproxy-service.yaml`

### 5. Frontend App

`kubectl apply -f k8s/frontend-deployment.yaml`

`kubectl apply -f k8s/frontend-service.yaml`
