# .NET MVC Application Deployment on Kubernetes with Minikube

This repository provides a step-by-step guide and configuration files for deploying a basic .NET MVC application on a local Kubernetes cluster using Minikube. The deployment includes setting up a MySQL database with persistent volumes, exposing the application as a service, and utilizing Kubernetes secrets for authentication credentials.

## Prerequisites

Before you begin, make sure you have the following tools installed:

- [Minikube](https://minikube.sigs.k8s.io/docs/start/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)

## Getting Started

1. **Clone the Repository**: Begin by cloning this repository to your local machine:

   ```bash
   git clone https://github.com/your-username/your-repo.git
   cd your-repo
2. Start Minikube
    ```bash
    minikube start

3. Apply Kubernetes Configurations: Deploy the application and MySQL container using the provided configuration files:
   ```bash
   kubectl apply -f mssql-secret.yaml
   kubectl apply -f mvcStore-deploy.yaml
   kubectl apply -f mvcservice.yaml
   kubectl apply -f mysql-deploy.yaml
   kubectl apply -f mssql-pv.yaml
4. Monitor Deployment : Keep an eye on the deployment progress by checking the status of the pods:
   ```bash
   kubectl get pods -w

   

