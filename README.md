🔐 Integrating Automated Security Scanning into DevOps Pipelines with SonarQube and Trivy

This project focuses on integrating automated security scanning and code quality analysis into DevOps pipelines using *SonarQube* for static code analysis and *Trivy* for container vulnerability scanning. The goal is to ensure *secure, high-quality, and production-ready applications* with continuous feedback during development and deployment phases.

---

## 📌 Table of Contents

* About the Project
* Team Roles
* Tech Stack
* Architecture
* Features
* Getting Started
* CI/CD & Security Integration
* Screenshots
* License

---

## 📖 About the Project

In this project, we:

* Implemented *SonarQube* for code quality and security analysis.
* Integrated *Trivy* to scan Docker images for vulnerabilities.
* Embedded security scans into *CI/CD pipelines* using GitHub Actions.
* Configured pipelines to *fail on high/critical vulnerabilities*.
* Visualized scan results and ensured *developer-friendly feedback loops*.
* Ensured compliance with DevSecOps principles for secure delivery.

---

## 👥 Team Roles

| Member       | Role                            | Responsibilities                                             |
| ------------ | ------------------------------- | ------------------------------------------------------------ |
| Mukesh K     | DevSecOps Engineer              | Designed the secure DevOps workflow and integrated tools     |
| Deepak       | CI/CD Engineer                  | Developed GitHub Actions workflows and pipeline integrations |
| Kumaresan    | Static Code Analysis Specialist | Set up and managed SonarQube scans and dashboards            |
| Mithra Varun | Container Security Engineer     | Integrated and automated Trivy for container scanning        |

---

## 🛠 Tech Stack

* *SonarQube* (Static Code Analysis)
* *Trivy* (Container Image Vulnerability Scanner)
* *Docker* (Containerization)
* *GitHub Actions* (CI/CD)
* *Kubernetes* (optional deployment)
* *GitHub* (Version Control)

---

## 🏗 Architecture


Developer Pushes Code
        |
        v
GitHub Repository --> GitHub Actions CI/CD Pipeline
        |
        |--> SonarQube Code Scan
        |
        |--> Build Docker Image
        |
        |--> Trivy Image Scan
        |
        |--> Deploy to Kubernetes (optional)


---

## ✅ FEATURES

👉 Integrated *SonarQube* for code smells, bugs, and security hotspots
👉 Automated *Trivy* scans for container vulnerabilities
👉 GitHub Actions fail builds on *critical/high vulnerabilities*
👉 Centralized *scan reports* and *code quality dashboards*
👉 Lightweight and extensible CI/CD configuration
👉 *Shift-left security*: Catch issues early in development

---

## 🚀 GETTING STARTED

### Prerequisites

👉 Docker
👉 GitHub Account
👉 GitHub Actions enabled
👉 SonarQube Server (local or cloud)
👉 Trivy CLI

### Clone the Repository

bash
git clone https://github.com/your-username/your-repo-name.git  
cd your-repo-name  


### Set up SonarQube (locally)

bash
docker run -d --name sonarqube -p 9000:9000 sonarqube  


### Install Trivy

bash
brew install aquasecurity/trivy/trivy   # macOS  
sudo apt install trivy                  # Ubuntu  


---

## 🔄 CI/CD & Security Integration

👉 *GitHub Actions Workflow*

* build.yml: Runs on push, triggers SonarQube scan and builds image
* security-scan.yml: Runs Trivy on the built image and checks for CVEs

👉 *SonarQube Integration*

* Sonar token and project key in GitHub Secrets
* Automatic PR comments for issues

👉 *Trivy Integration*

* Fail builds if image has CRITICAL or HIGH vulnerabilities
* JSON reports exported for auditing

---

## 🖼 Screenshots

* SonarQube Dashboard with Quality Gates
* GitHub Actions Logs for Trivy and Sonar Scans
* Trivy Report Sample
* Code Annotations from Sonar PR Comments

---

## 📄 License

MIT License. Feel free to use and contribute.
