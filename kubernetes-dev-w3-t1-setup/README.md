# DEV-W3-T1 – Provision Kubernetes Environment

## Tools
- Minikube
- kubectl
- Kubernetes

## Steps

### 1. Start Minikube
```
minikube start
```

### 2. Create Namespaces
```
kubectl apply -f namespaces/
```

### 3. Deploy Backend
```
kubectl apply -f backend/backend-deployment.yaml
```

### 4. Expose Backend Service
```
kubectl apply -f backend/backend-service.yaml
```

### 5. Verify
```
kubectl get namespaces
kubectl get pods -n backend
kubectl get svc -n backend
```

### 6. Access Application
```
minikube service backend-service -n backend
```
