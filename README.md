# Widgetario Hackathon

## 🧩 Overview

**Widgetario Hackathon** is a Kubernetes-based microservices project designed to demonstrate scalable deployments, monitoring, and automation. This repository includes all necessary files and instructions for setup, usage, testing, and deployment.

---

## 📁 Repository Structure

- `/k8s`: Kubernetes manifests for deployments, services, and configurations  
- `/docs`: Documentation related to the project  


---

## ⚙️ Installation Instructions

Clone the repository and navigate into it:

```bash
git clone https://github.com/Njihia097/Widgetario-hackathon.git
cd Widgetario-hackathon
```

---

## ☸️ Kubernetes Setup

Ensure you have `kubectl` and **Minikube** (or any Kubernetes cluster) installed. Then deploy the core components:

```bash
kubectl apply -k k8s/core
```

This will deploy the following:
- **Products API**
- **Stock API**
- **PostgreSQL Database**

---

## 🚀 Usage Guidelines

To run and interact with the services:

```bash
kubectl get pods
kubectl port-forward svc/products-api 8080:80
```

Then access the API at:  
👉 [http://localhost:8080](http://localhost:8080)

---

## 📚 Code Documentation

- Follows consistent naming conventions.
- Key functions are documented with inline comments.
- Core logic is explained clearly within the source files.

---

## ✅ Testing

Run the test cases to validate functionality:

```bash
kubectl apply -k k8s/tests
```

More detailed instructions are available in the `/tests` directory.

---

## 🚢 Deployment Instructions

To deploy the full system including ingress:

1. Set up required environment variables.
2. Apply the ingress configuration:

```bash
kubectl apply -k k8s/ingress
```

Then access the services via:  
👉 [http://widgetario.local](http://widgetario.local)

---

