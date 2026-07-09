# Container Security Pipeline using Docker, Trivy & GitHub Actions

## Project Overview

This project demonstrates how to integrate container vulnerability scanning into a CI/CD pipeline using Docker, Trivy, and GitHub Actions.

The pipeline automatically builds a Docker image and scans it for security vulnerabilities before deployment.

---

## Technologies Used

- Docker
- Trivy
- GitHub Actions
- Git
- VS Code

---

## Project Structure

```
container-security-pipeline/
│
├── .github/
│   └── workflows/
│       └── security.yml
├── Dockerfile
├── index.html
├── README.md
└── report.json
```

---

## Docker Build

```bash
docker build -t security-demo .
```

---

## Run Container

```bash
docker run -d -p 8081:80 --name security-demo-container security-demo
```

Open:

```
http://localhost:8081
```

---

## Scan with Trivy

```bash
trivy image security-demo
```

Generate JSON Report

```bash
trivy image --format json -o report.json security-demo
```

---

## GitHub Actions Workflow

The GitHub Actions pipeline performs the following tasks:

- Checkout Repository
- Build Docker Image
- Scan Docker Image using Trivy
- Fail the workflow if HIGH or CRITICAL vulnerabilities are found

---

## Skills Demonstrated

- Docker Containerization
- Container Security
- Vulnerability Scanning
- DevSecOps
- GitHub Actions CI/CD
- Secure Software Delivery

---

## Author

**Padmakar Joshi**