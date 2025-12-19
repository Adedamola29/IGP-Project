# ABC Technologies – CI/CD DevOps Pipeline Project

## 📌 Project Overview
ABC Technologies is a leading online retail organization that recently acquired a large offline retail business. The acquired system relied on traditional development and deployment methods, resulting in low availability, poor scalability, performance issues, and slow release cycles.

This project implements a **DevOps-based CI/CD pipeline** to automate the build, test, packaging, and deployment of a Java web application, significantly improving reliability, scalability, and time to market.

---

## 🎯 Project Objectives
The main goals of this project are to:
- Implement Continuous Integration and Continuous Deployment (CI/CD)
- Improve application availability and scalability
- Reduce manual intervention and deployment errors
- Enable faster and more frequent releases
- Ensure consistent and repeatable deployments

---

## 🏗️ CI/CD Architecture Flow
1. Developer pushes source code to **GitHub**
2. **Jenkins** pulls the code and performs:
   - Compilation
   - Unit testing
   - Packaging (WAR file)
3. **Docker** builds a container image using Tomcat and the WAR file
4. **Ansible** automates deployment by:
   - Stopping old containers
   - Removing outdated images
   - Building a fresh Docker image
   - Running the application container on EC2
5. Application is accessed via browser on the EC2 public IP

---

## 🛠️ Tools & Technologies Used
- **AWS EC2** – Infrastructure hosting
- **GitHub** – Source code management
- **Jenkins** – Continuous Integration
- **Maven** – Build and dependency management
- **Docker** – Containerization
- **Ansible** – Automated deployment and configuration management
- **Linux (Ubuntu)** – Operating system

---

## 📂 Project Structure
IGP-Project/
│
├── src/
├── pom.xml
├── Dockerfile
├── ansible/
│ ├── hosts.ini
│ └── deploy-abc-app.yml
└── README.md


---

## ⚙️ Jenkins Pipeline Stages
- **Compile Stage**
- **Test Stage**
- **Package Stage**

---

## 🐳 Docker Containerization
The application is packaged into a Docker image using **Tomcat** and deployed as a container to ensure consistency across environments.

---

## 🤖 Role of Ansible
Ansible automates deployment by stopping old containers, removing outdated images, rebuilding the Docker image, and running the latest version of the application.

---

## 🚀 Application Access
http://18.221.206.169:8081/


---

## ✅ Conclusion
This project demonstrates a complete CI/CD DevOps pipeline using Jenkins, Docker, and Ansible to deliver a scalable, automated, and reliable application deployment solution.



