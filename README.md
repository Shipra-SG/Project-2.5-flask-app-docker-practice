# Flask App Docker Practice

This repository contains a simple **Flask web application** containerized using **Docker** as part of my hands-on DevOps practice.

In this project, I learned how to:

* Write a Dockerfile for a Python Flask application
* Build a Docker image
* Run the image as a container
* Understand how Docker containerizes a web app

---

## Project Overview

This Flask application displays a simple webpage when accessed. The focus of this project is not the application logic, but understanding how to use Docker to package and run Python applications.

---

## 🛠 Tech Stack

| Technology | Purpose                             |
| ---------- | ----------------------------------- |
| Python     | Core language for the Flask app     |
| Flask      | Web framework                       |
| Docker     | Containerization                    |
| Git        | Source control                      |
| Linux      | Development/execution environment |

---

## Dockerfile Explained

### What each line does:

```dockerfile
FROM python:3.9-alpine
```
🔹 Uses a lightweight Python image

```dockerfile
WORKDIR /app
```
🔹 Sets working directory inside container

```dockerfile
COPY requirements.txt ./
```
🔹 Copies dependency list

```dockerfile
RUN pip install --no-cache-dir -r requirements.txt
```
✅ Installs Python packages (Flask, etc.)

```dockerfile
COPY . .
```
🔹 Copies application code into the container

```dockerfile
CMD ["python", "app.py"]
```
▶ Starts the Flask app

---

## How to Use This Project

### 1️⃣ Clone the Repository

```bash
git clone <repo-URL>
cd <Project>
```

---

### 2️⃣ Build the Docker Image

```bash
docker build -t flask-docker-app .
```

---

### 3️⃣ Run the Container

```bash
docker run -d -p 5000:5000 flask-docker-app
```

Now open your browser and visit:

```
http://<public-IP>:5000
```
You should see the simple Flask app response.

---

## Learning Outcomes

Through this project, I learned:

* How to write a Dockerfile for a Python app
* How containers isolate app runtimes
* How to build and run images and containers
* How web apps listen on a port inside containers

---

## Additional Notes

* This project uses **Flask**, a lightweight Python web framework
* Used `python:3.9-alpine` for a small image
* Learned how container ports map to host ports

---

## Why This Matters

As a DevOps learner, containerizing applications is an essential skill before moving into:

* Kubernetes deployment
* CI/CD pipelines
* Cloud-based deployments (AWS, EKS, etc.)

---

## 👩‍💻 Author

**Shipra**
DevOps & Cloud Enthusiast 🌱
Practicing Docker → Kubernetes → AWS
