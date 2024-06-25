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

### Accessing the Application

External Services (NodePort)
Voting Application: Accessible via http://<minikube_ip>:30004
Result Application: Accessible via http://<minikube_ip>:30005

To get the IP address of Minikube:

```
minikube ip
```

### Testing the Application

Access the Voting Application in your web browser using the provided URL.
Cast a vote (e.g., select "Dogs") and verify that it reflects in the Result Application.
Access the Result Application to view the voting results.



