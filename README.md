# 📦 Flask App: Dockerized and Deployed on Kubernetes

This project demonstrates how to containerize a basic **Flask web application** and deploy it on a **Kubernetes cluster**. The deployment is cloud-based (hosted on **Amazon EC2**) and accessible externally.

---

## 🚀 Tech Stack

- **Python / Flask** – Web framework  
- **Docker** – Containerization  
- **Kubernetes** – Orchestration  
- **kubectl** – Kubernetes CLI  
- **Amazon EC2 (Ubuntu)** – Cloud host for deployment  
- **(Optional)** Helm – Initialized but not used

---


---

## 🐳 Docker Instructions

Build and run locally:

```bash
docker build -t flask-app .
docker run -p 5000:5000 flask-app


kubectl apply -f k8s/configmap.yaml
kubectl apply -f k8s/secret.yaml
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml

for access
http://<EC2-PUBLIC-IP>:30080
