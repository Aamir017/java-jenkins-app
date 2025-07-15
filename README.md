# ☕ Java Jenkins CI/CD Demo App

This is a minimal Spring Boot web application used to demonstrate a full CI/CD pipeline using **Jenkins**, **Docker**, and **DockerHub**. It prints a simple response via a REST API.

---

## 📌 Tech Stack

- Java 17
- Spring Boot 3
- Maven
- Docker (Multi-stage)
- Jenkins (Freestyle Job)
- DockerHub

---

## ✅ Features

- Simple REST endpoint: `GET /` → returns `Hello from single-file Jenkins CI/CD Java App!`
- Dockerized with a multi-stage Dockerfile
- CI/CD pipeline using Jenkins:
  - Pull code from GitHub
  - Build JAR with Maven
  - Build and push Docker image to DockerHub

---

## 🏗️ Project Structure

java-jenkins-app/
├── src/
│ └── main/
│ └── java/com/example/demo/
│ ├── DemoApplication.java
│ └── HelloController.java
├── pom.xml
├── Dockerfile
└── .dockerignore (optional)

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/aamir017/java-jenkins-app.git
cd java-jenkins-app
```
### 2. Build & Run Locally
```bash
# Build JAR
mvn clean package -DskipTests

# Run app
java -jar target/java-jenkins-app-0.0.1-SNAPSHOT.jar
```
Visit: http://localhost:8080

### 3. Docker Build & Run
```bash
# Build Docker image
docker build -t <your-dockerhub-username>/java-jenkins-app .

# Run container
docker run -p 8080:8080 <your-dockerhub-username>/java-jenkins-app
```

### 4. Jenkins CI/CD Pipeline Overview
Freestyle Job Steps:

Clone code from GitHub

Run mvn clean package -DskipTests

Build Docker image:
docker build -t <dockerhub-username>/java-jenkins-app .

Push to DockerHub:

```bash
docker login -u $DOCKERHUB_USER -p $DOCKERHUB_PASS
docker push <dockerhub-username>/java-jenkins-app
```
Make sure to set DOCKERHUB_USER and DOCKERHUB_PASS as Jenkins credentials.

🐳 DockerHub
The image gets pushed to:
https://hub.docker.com/r/your-dockerhub-username/java-jenkins-app


🙌 Author
🙌 Author  

Built by **Aamir017** using DevOps tools from scratch!  

GitHub: [github.com/Aamir017](https://github.com/Aamir017)  
DockerHub: [hub.docker.com/u/Aamir017](https://hub.docker.com/u/Aamir017)

