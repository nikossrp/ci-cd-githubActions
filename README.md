# Java Spring Boot Hello World App with CI/CD Pipeline

This is a simple Java Spring Boot web application that returns a "Hello World" message. The project demonstrates a complete **CI/CD pipeline** using **GitHub Actions** to build, test, and deploy a Docker image to Docker Hub.

---

## Project Structure

```
.
├── .github
│   └── workflows
│       └── ci.yml      # GitHub Actions workflow file for CI/CD
├── Java_project        # Spring Boot application source code
│   └── demo
│       └── demo
│           ├── Dockerfile  # Dockerfile to build the app image
│           ├── pom.xml
│           └── src    

```

---

## Features

- Built with **Java 17** and **Spring Boot**
- Uses **Maven** for build and dependency management
- Dockerized application for easy deployment
- Automated **CI/CD pipeline** using GitHub Actions
- Docker image pushed to **Docker Hub**

---

## How to Build and Run Locally

### Prerequisites

- Java 17 JDK installed
- Maven installed
- Docker installed

### Build and Run with Maven

```bash
cd Java_project/demo/demo
./mvnw clean package
java -jar target/demo-0.0.1-SNAPSHOT.jar
```

The application will start on `http://localhost:8080`.

### Build and Run with Docker

Build Docker image locally:

```bash
docker build -t nickdev98/java-hello-world .
```

Run the container:

```bash
docker run -p 8080:8080 nickdev98/java-hello-world
```

Open `http://localhost:8080` in your browser.

---

## CI/CD Pipeline

This project uses GitHub Actions to:

- Build the project with Maven
- Build the Docker image
- Push the Docker image to Docker Hub (`nickdev98/spring-hello-world`)

Workflow file is located at `.github/workflows/ci.yml`.

---

## Docker Hub

Docker image is available on Docker Hub:

[https://hub.docker.com/r/nickdev98/spring-hello-world](https://hub.docker.com/r/nickdev98/spring-hello-world)

---

