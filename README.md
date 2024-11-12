# ----- NGINX INGRESS CONTROLLER ------

Installing NGINX Ingress Controller on Amazon EKS

The NGINX Ingress Controller is a popular choice for managing traffic in Kubernetes environments. Here's a step-by-step guide on how to install it on your Amazon EKS cluster using Helm.

Prerequisites:
An existing Amazon EKS cluster.
kubectl: Configured to connect to your cluster.
Helm: Installed and configured.
Installation Steps:
Add the NGINX Ingress Controller Helm Chart Repository:

Bash
helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
helm repo update
Use code with caution.

Install the NGINX Ingress Controller:   

Bash
helm install ingress-nginx ingress-nginx/ingress-nginx \
  --namespace ingress-nginx
Use code with caution.

Verifying the Installation:
Check the Deployment:
Bash
kubectl get deployments -n ingress-nginx
Use code with caution.

Check the Service:
Bash
kubectl get svc -n ingress-nginx
Use code with caution.

