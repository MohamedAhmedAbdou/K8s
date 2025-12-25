# EKS Project

This project demonstrates setting up an **EKS (Elastic Kubernetes Service)** cluster on AWS using Terraform and deploying applications using Docker images from Docker Hub.

---

## 📌 Overview
The project covers:  
- Creating an **EKS cluster** using Terraform (from the previous repo setup)  
- Deploying a **Node.js application** (built from previous repository) as a Docker image pulled from **Docker Hub**  
- Deploying an **Nginx Docker image** also pulled from **Docker Hub**  
- Setting up **two ClusterIP services** to expose the pods internally  
- Configuring an **Ingress Load Balancer** to expose the services externally  
- Installing an **Ingress Controller** to manage ingress traffic  

---

## 🛠 Tools & Technologies
- AWS EKS  
- Terraform  
- Kubernetes (Pods, Services, Ingress)  
- Docker / Docker Hub  
- Node.js application  

---

## ⚙️ Kubernetes Setup

### 1️⃣ Pods
- Main pod runs the **Node.js application Docker image**  
- Auxiliary pod runs the **Nginx Docker image**  

### 2️⃣ Services
- Two services of type **ClusterIP** for internal communication  
- Expose pods internally within the cluster  

### 3️⃣ Ingress
- Configured **Ingress Load Balancer** on top of the services  
- Routes external traffic to internal services  
- Managed by **Ingress Controller**  

---

## 🚀 Deployment Flow
1. Terraform scripts create the **EKS cluster**  
2. Kubernetes manifests deploy the **Node.js Docker image** and **Nginx Docker image**  
3. Services and ingress are applied  
4. External traffic can access the Node.js app via the load balancer  

---

## 📄 Notes
- Both Docker images are pulled from **Docker Hub**  
- The Node.js app Docker image was **built from the previous repository**  
- This setup can be extended with **CI/CD pipelines** and **Helm charts** for better management  
