
---

# Kubernetes Test Application (Flask)

This is a simple Flask web application built to demonstrate containerization with Docker and deployment testing using Minikube Kubernetes. The application accepts a name from the user and returns a greeting message.

---

## 🚀 Features

* Lightweight Flask web app
* Containerized using Docker
* Deployed and tested successfully on Minikube
* Single Kubernetes manifest file (`deployment.yaml`) containing both Deployment and Service

---

## 📁 Project Structure

```
.
├── app.py
├── deployment.yaml        # Contains both Deployment & Service
├── templates/
│   └── index.html
├── static/
│   └── style.css
└── Dockerfile
```

---

## ▶️ Running Locally

### Install dependencies

```bash
pip install flask
```

### Start the application

```bash
python app.py
```

The app will be available at: **[http://0.0.0.0:5000](http://0.0.0.0:5000)**

---

## 🐳 Docker Usage

### Build the Docker image

```bash
docker build -t k8s-app-test .
```

### Run the container

```bash
docker run -p 5000:5000 k8s-app-test
```

---

## ☸️ Kubernetes (Minikube) Deployment

### Start Minikube

```bash
minikube start
```

### Load the image into Minikube

```bash
minikube image load k8s-app-test
```

### Apply the combined Deployment + Service manifest

```bash
kubectl apply -f deployment.yaml
```

### Access the application

```bash
minikube service k8s-app-test
```

---

## ✅ Status

* Flask app working locally ✔️
* Docker container tested successfully ✔️
* Minikube deployment validated using a single manifest ✔️

---
