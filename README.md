# 🌐 AWS Application Load Balancer with EC2 – Hands-on Project

## 📌 Project Overview
This project demonstrates how to deploy an **Amazon EC2 instance** and connect it to an **AWS Application Load Balancer (ALB)** to achieve **high availability, scalability, and fault tolerance**.

The repository explains the **end-to-end setup process**, the **working of the load balancer**, and key **AWS concepts** involved.

This project is designed for **beginners** who want practical exposure to **AWS networking and traffic management**.

---

## 🎯 Objectives
- Understand the role of an **Application Load Balancer**
- Learn how traffic is distributed to backend **EC2 instances**
- Configure **Target Groups** and **Health Checks**
- Verify load balancer functionality using the **ALB DNS name**
- Gain real-world **AWS troubleshooting experience**

---

## 🛠️ Technologies & Services Used
- Amazon EC2  
- Application Load Balancer (ALB)  
- Target Groups  
- Security Groups  
- Amazon VPC & Subnets  
- HTTP (Port 80)  

---

## 🏗️ Architecture Overview
The ALB continuously checks the **health of the EC2 instance** and forwards traffic **only to healthy targets**.

---

## 🚀 Step-by-Step Implementation

### 1️⃣ Launch an EC2 Instance
- Create an EC2 instance using **Amazon Linux**
- Install and start a web server (Apache)
- Deploy a simple HTML webpage
- Ensure the instance is running

---

### 2️⃣ Configure Security Groups
- Allow **HTTP (Port 80)** from the Load Balancer
- Allow **SSH (Port 22)** for administrative access

---

### 3️⃣ Create a Target Group
- Target type: **Instance**
- Protocol: **HTTP**
- Port: **80**
- Register the EC2 instance
- Verify that the instance health status is **Healthy**

---

### 4️⃣ Create an Application Load Balancer
- Select **Application Load Balancer**
- Use **public subnets**
- Configure a listener on **Port 80**
- Attach the previously created target group

---

### 5️⃣ Verify the Setup
- Copy the **ALB DNS name**
- Open it in a browser
- Confirm that the **EC2-hosted webpage loads successfully**

---

## 🔍 How the Load Balancer Works
- The ALB receives incoming **HTTP requests**
- It evaluates **listener rules**
- Traffic is routed only to **healthy targets**
- **Health checks** continuously monitor
