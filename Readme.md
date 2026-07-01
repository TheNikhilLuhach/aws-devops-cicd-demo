# 🚀 AWS DevOps CI/CD Pipeline Demo

A complete CI/CD pipeline project built using **AWS EC2**, **Jenkins**, **GitHub**, and **Apache HTTP Server**. This project demonstrates how code changes pushed to GitHub are automatically built and deployed to an AWS EC2 instance using Jenkins.

---

# 📌 Project Overview

This project showcases a simple DevOps CI/CD workflow where a static website is automatically deployed whenever changes are pushed to the GitHub repository.

The pipeline performs the following tasks:

- Fetches source code from GitHub
- Builds the project
- Deploys website files to Apache Web Server
- Verifies successful deployment
- Displays the updated website automatically

---

# 🏗️ Architecture

```
                 +----------------+
                 |   GitHub Repo  |
                 +--------+-------+
                          |
                     Git Push
                          |
                          ▼
                 +----------------+
                 |    Jenkins      |
                 |  CI/CD Pipeline |
                 +--------+--------+
                          |
                 Checkout Source Code
                          |
                     Build Project
                          |
                    Deploy Website
                          |
                          ▼
                +-------------------+
                | Apache Web Server |
                |     AWS EC2       |
                +-------------------+
                          |
                          ▼
                   Static Website
```

---

# 🛠️ Technologies Used

- AWS EC2 (Amazon Linux 2023)
- Jenkins
- Git
- GitHub
- Apache HTTP Server (httpd)
- HTML5
- CSS3
- Linux
- Shell Commands

---

# 📂 Project Structure

```
aws-devops-cicd-demo/
│
├── Jenkinsfile
├── index.html
├── style.css
└── README.md
```

---

# ⚙️ Jenkins Pipeline Stages

## Stage 1 – Checkout Source

Downloads the latest code from GitHub.

---

## Stage 2 – Build

Builds the project and verifies project files.

---

## Stage 3 – Deploy

Copies website files to Apache Web Server directory.

```
/var/www/html/
```

---

## Stage 4 – Verify

Verifies deployment and ensures the website is available.

---

# 📜 Jenkinsfile Workflow

```
Checkout Code
      ↓
Build Project
      ↓
Deploy Website
      ↓
Verify Deployment
      ↓
Pipeline Success
```

---

# 🚀 Deployment Steps

### 1. Launch AWS EC2 Instance

- Amazon Linux 2023
- Open Port 22
- Open Port 80
- Open Port 8080

---

### 2. Install Java

```bash
sudo dnf install java-17-amazon-corretto -y
```

---

### 3. Install Jenkins

```bash
sudo wget -O /etc/yum.repos.d/jenkins.repo \
https://pkg.jenkins.io/redhat-stable/jenkins.repo

sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key

sudo dnf install jenkins -y
```

---

### 4. Start Jenkins

```bash
sudo systemctl enable jenkins
sudo systemctl start jenkins
```

---

### 5. Install Apache

```bash
sudo dnf install httpd -y

sudo systemctl enable httpd

sudo systemctl start httpd
```

---

### 6. Install Git

```bash
sudo dnf install git -y
```

---

### 7. Configure Jenkins

- Install Suggested Plugins
- Create Admin User
- Install Git Plugin
- Configure GitHub Repository

---

### 8. Create Pipeline Job

Pipeline Type

```
Pipeline Script from SCM
```

SCM

```
Git
```

Repository URL

```
https://github.com/TheNikhilLuhach/aws-devops-cicd-demo.git
```

Branch

```
main
```

Script Path

```
Jenkinsfile
```

---

### 9. Run Pipeline

Click

```
Build Now
```

---

### 10. Verify Website

Open Browser

```
http://<EC2-Public-IP>
```

Example

```
http://18.xx.xx.xx
```

---

# 📷 Project Output

✔ Jenkins Pipeline Successful

✔ GitHub Repository Connected

✔ Automatic Deployment

✔ Website Hosted on AWS EC2

✔ Apache Server Running

---

# 📈 CI/CD Workflow

```
Developer
    │
    ▼
GitHub Push
    │
    ▼
Jenkins Detects Change
    │
    ▼
Checkout Code
    │
    ▼
Build
    │
    ▼
Deploy
    │
    ▼
Apache Web Server
    │
    ▼
Live Website
```

---

# ✅ Features

- Jenkins CI/CD Pipeline
- Automatic Deployment
- GitHub Integration
- AWS EC2 Hosting
- Apache Web Server
- Static Website Deployment
- Linux Based Deployment
- Continuous Integration
- Continuous Delivery

---

# 📚 Learning Outcomes

Through this project, I learned:

- Jenkins Installation
- GitHub Integration
- Pipeline Creation
- Continuous Integration
- Continuous Deployment
- Apache Configuration
- AWS EC2 Management
- Linux Commands
- Git Workflow
- DevOps Basics

---

# 👨‍💻 Author

**Nikhil Kumar**

DevOps Intern

GitHub:
https://github.com/TheNikhilLuhach

LinkedIn:
https://www.linkedin.com/

---

# ⭐ If you found this project useful

Please consider giving this repository a ⭐ on GitHub.
