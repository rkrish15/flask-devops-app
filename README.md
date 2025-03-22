Here's a clean and to-the-point `README.md` file without any extra formatting:  

---

### **README.md**  

```md
# Flask DevOps App  

This project is a simple Flask web application that is containerized using Docker and deployed on Kubernetes.  

## Prerequisites  
- Docker  
- Minikube  
- kubectl  

## Project Files  
- **app.py** – Flask application source code  
- **Dockerfile** – Docker configuration file  
- **deployment.yaml** – Kubernetes Deployment manifest  
- **service.yaml** – Kubernetes Service manifest  

## Steps to Run  

### 1. Clone the Repository  
```sh
git clone https://github.com/rkrish15/flask-devops-app.git
cd flask-devops-app
```

### 2. Build and Run the Docker Container  
```sh
docker build -t flask-app:latest .
docker run -p 5000:5000 flask-app
```

### 3. Deploy to Kubernetes  

#### Start Minikube  
```sh
minikube start
```

#### Load Docker Image into Minikube  
```sh
eval $(minikube docker-env)
docker build -t flask-app:latest .
```

#### Apply Kubernetes Configurations  
```sh
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

### 4. Access the Application  
Find the NodePort using:  
```sh
minikube service flask-app-service --url
```
Open the provided URL in a web browser to see the response:  
```
Welcome to DevOps Flask App!
```

## Deliverables  
- Flask app source code (`app.py`)  
- Dockerfile  
- Kubernetes manifests (`deployment.yaml`, `service.yaml`)  
- Screenshot of the app running  
- GitHub repository link  

## GitHub Repository  
[https://github.com/rkrish15/flask-devops-app](https://github.com/rkrish15/flask-devops-app)  
```
