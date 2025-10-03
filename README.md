# AWS EC2 Apache Demo 🚀

This project demonstrates how to **launch an AWS EC2 instance**, install **Apache HTTP server**, and host a simple webpage.  

---

## 📌 Architecture
- **AWS EC2** (Amazon Linux 2023)
- **Apache HTTPD** (Web Server)
- **Security Group** with inbound rules:
  - **Port 22 (SSH)** → to connect via terminal  
  - **Port 80 (HTTP)** → to allow browser access  

---

## ⚙️ Steps Followed

### 1. Launch EC2 Instance
- Selected **Amazon Linux 2023 AMI**
- Instance type: **t2.micro (Free Tier)**
- Created key pair (`.pem`) for SSH login
- Configured **security group** to allow:
  - SSH (22) from my IP  
  - HTTP (80) from anywhere (`0.0.0.0/0`)

---

### 2. Connect to Instance
```bash
ssh -i "ayush-key.pem" ec2-user@<PUBLIC_IP>
