# k8s_sample_project
This is sample project for beginners who want to understand the kubernetes 

#Minikube expose service command
minikube service django-service

# Port Forwarding NGINX Ingress Controller
kubectl port-forward svc/ingress-nginx-controller 8080:80 -n ingress-nginx

# Basic kubectl Commands
kubectl get pods
kubectl get nodes
kubectl get svc
kubectl describe pod <pod-name>
kubectl logs <pod-name>
kubectl apply -f <file.yaml>
kubectl delete pod <pod-name>

# Exposing Services in Kubernetes
kubectl expose deployment <deployment-name> --type=LoadBalancer --port=80 --target-port=8080
kubectl expose deployment <deployment-name> --type=NodePort --port=80 --target-port=8080

# Ingress Setup
kubectl apply -f ingress.yaml
kubectl get ingress
kubectl describe ingress <ingress-name>

# Port Forwarding to Access Services
kubectl port-forward svc/<service-name> <local-port>:<service-port>
kubectl port-forward pod/<pod-name> <local-port>:<container-port>
