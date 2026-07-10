# 🚀 Complete DevOps CI/CD Pipeline Project - Clone Netflix

### GitHub → Jenkins → Maven → Apache Tomcat → Prometheus → Grafana

---

# 📖 Project Overview

This project demonstrates a complete End-to-End DevOps CI/CD pipeline for deploying a **Clone Netflix Java Web Application** using industry-standard DevOps tools.

Whenever a developer pushes code to the GitHub repository, GitHub automatically triggers Jenkins through a Webhook. Jenkins checks out the latest source code, builds the application using Maven, and deploys the generated WAR file to Apache Tomcat. The deployed application and server infrastructure are continuously monitored using Prometheus and Grafana.

This project showcases a real-world CI/CD workflow, automating the entire software delivery lifecycle—from source code management to deployment and monitoring.

---

# 🎯 Project Objectives

- Automate the build and deployment process using Jenkins.
- Integrate GitHub with Jenkins using GitHub Webhooks.
- Build the Java application using Apache Maven.
- Deploy the generated WAR file to Apache Tomcat.
- Monitor server performance with Prometheus.
- Visualize infrastructure metrics using Grafana.
- Demonstrate a complete CI/CD pipeline on AWS EC2.

---

# 📋 Implementation Steps

### Step 1: Launch AWS EC2 Instance
- Create an Ubuntu EC2 instance.
- Configure Security Groups to allow ports:
  - **22** (SSH)
  - **8080** (Jenkins/Tomcat)
  - **9090** (Prometheus)
  - **3000** (Grafana)

---

### Step 2: Install Required Software

Install the following tools on the EC2 instance:

- Java JDK 17
- Git
- Jenkins
- Apache Maven
- Apache Tomcat
- Prometheus
- Grafana
- Node Exporter

---

### Step 3: Create GitHub Repository

- Create a GitHub repository.
- Upload the Clone Netflix Java application.
- Push the source code to the `main` branch.

---

### Step 4: Configure Jenkins

- Install the required Jenkins plugins.
- Configure JDK and Maven.
- Create a Jenkins job.
- Connect the GitHub repository.
- Configure the build steps.

---

### Step 5: Configure GitHub Webhook

- Add the Jenkins webhook URL in the GitHub repository.
- Enable **Push Events**.
- Verify webhook delivery.

---

### Step 6: Trigger the CI Pipeline

When the developer executes:

```bash
git add .
git commit -m "Added new feature"
git push origin main
```

GitHub automatically triggers the Jenkins pipeline.

---

### Step 7: Build the Application

Jenkins performs the following tasks:

- Checkout source code
- Download dependencies
- Compile the project
- Run Maven build
- Generate the WAR file

---

### Step 8: Deploy the Application

After a successful build:

- Copy the WAR file to Apache Tomcat.
- Restart Tomcat (if required).
- Verify that the Clone Netflix application is running.

---

### Step 9: Monitor the Infrastructure

Prometheus continuously collects metrics such as:

- CPU Usage
- Memory Usage
- Disk Usage
- Network Traffic
- JVM Metrics

---

### Step 10: Visualize Metrics

Grafana connects to Prometheus and displays real-time dashboards for:

- System Health
- CPU Utilization
- Memory Consumption
- Disk Space
- Network Monitoring
- Application Performance

---

### Architecture Workflow

```
                 👨‍💻 Developer
                       │
                 Push Code
                       │
                       ▼
                  GitHub Repository
                       │
                GitHub Webhook
                       │
                       ▼
                    Jenkins
                       │
             Build using Maven
                       │
                       ▼
                Apache Tomcat
                       │
                       ▼
          Netflix Clone Application
                       │
                       ▼
                 Prometheus
                       │
                       ▼
                   Grafana
```

---

# 🏗️ Project Architecture

> Add your architecture diagram here.

![Project Architecture](https://github.com/rushikeshsatwadhar/java-project/blob/main/Screenshot/Project%20Architecture.png?raw=true)

---

---

# 📸 Project Outputs

## Step 1: AWS EC2 Instance

An Ubuntu EC2 instance was launched to host Jenkins, Tomcat, Prometheus, Grafana, and the Netflix Clone application.

![AWS EC2](https://github.com/rushikeshsatwadhar/java-project/blob/main/Screenshot/AWS%20EC2%20Instance.png?raw=true)

---

## Step 2: Jenkins Dashboard

Jenkins was installed and configured as the Continuous Integration (CI) server. It automatically detects code changes from GitHub, builds the project using Maven, and deploys the application.

![Jenkins Dashboard](https://github.com/rushikeshsatwadhar/java-project/blob/main/Screenshot/Jenkins%20Dashboard.png?raw=true)

---

## Step 3: Deploy Application on Apache Tomcat

After a successful Maven build, Jenkins deployed the generated WAR file to Apache Tomcat.

![Tomcat](https://github.com/rushikeshsatwadhar/java-project/blob/main/Screenshot/Deploy%20Application%20on%20Apache%20Tomcat.png?raw=true)

---

## Step 4: Netflix Clone Application

The Java web application was successfully deployed and is accessible through the Tomcat server.

![Netflix Clone](https://github.com/rushikeshsatwadhar/java-project/blob/main/Screenshot/Netflix%20Clone%20Application.png?raw=true)

---

## Step 5: Prometheus Monitoring

Prometheus continuously collects infrastructure and application metrics from the server.

![Prometheus](https://github.com/rushikeshsatwadhar/java-project/blob/main/Screenshot/Prometheus%20Monitoring.png?raw=true)

---

## Step 6: Grafana Dashboard

Grafana connects to Prometheus and visualizes the collected metrics using interactive dashboards.

![Grafana](https://github.com/rushikeshsatwadhar/java-project/blob/main/Screenshot/Grafana%20Dashboard.png?raw=true)

---
