# Kubernetes HPA Project

This project demonstrates **Horizontal Pod Autoscaling (HPA)** in Kubernetes using
CPU-based metrics and load testing with **BusyBox**.

---

## Tech Stack
Kubernetes, Minikube, Metrics Server, BusyBox

---

## Files Used 
k8s/namespace.yml  
k8s/deployment.yml  
k8s/service.yml  
k8s/hpa.yml  
load-test/busybox-load-test.yml  

---

## Run Commands

minikube start  
minikube addons enable metrics-server  

kubectl apply -f k8s/namespace.yml  
kubectl apply -f k8s/deployment.yml  
kubectl apply -f k8s/service.yml  
kubectl apply -f k8s/hpa.yml  

kubectl apply -f load-test/busybox-load-test.yml  

---

## Verify HPA

kubectl get hpa -n apache  
kubectl get pods -n apache  
kubectl top pods -n apache  

Pods automatically scale up on high CPU load and scale down when load stops.

---

## Stop Load Test

kubectl delete pod busybox-load -n apache  

---

## Learning
Kubernetes Deployment & Service, HPA, Metrics Server, internal DNS,
load testing using BusyBox.

---

👨‍💻 Author

Meet Dangar DevOps & Cloud Enthusiast
