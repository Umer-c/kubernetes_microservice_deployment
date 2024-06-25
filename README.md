# kubernetes_microservice_deployment
This guide provides steps to deploy a multi-tier voting application on Minikube using Kubernetes YAML configuration files.

## Steps to Deploy

### Clone the Repository

Clone the repository containing the Kubernetes YAML files for deploying the application components.

### Deploy Pods

Deploy the Kubernetes Pods for each component of the application using kubectl create command.

```
kubectl create -f postgres_pod.yaml
kubectl create -f redis_pod.yaml
kubectl create -f worker_pod.yaml
kubectl create -f result_app_pod.yaml
kubectl create -f voting_app_pod.yaml
```

### Deploy Services

Deploy the Kubernetes Services to expose the Pods internally and externally using kubectl create command.

```
kubectl create -f postgres_service.yaml
kubectl create -f redis_service.yaml
kubectl create -f result_app_service.yaml
kubectl create -f voting_app_service.yaml
```
