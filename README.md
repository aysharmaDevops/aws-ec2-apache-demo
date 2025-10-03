AWS EC2 Apache Project 🚀

This project demonstrates how to:

Launch an EC2 instance

Connect via SSH

Install & configure Apache (httpd)

Serve a simple webpage

Verify using a browser

Document & push everything into GitHub

🔹 Steps Performed
1. Launch EC2 Instance

Chose Amazon Linux 2023 AMI.

Selected t2.micro (Free Tier).

Configured security group:

Port 22 (SSH) – open to My IP.

Port 80 (HTTP) – open to 0.0.0.0/0.

2. Connect via SSH
ssh -i "ayush-key.pem" ec2-user@<EC2-PUBLIC-IP>

3. Update System
sudo dnf update -y

4. Install Apache (httpd)
sudo dnf install -y httpd
sudo systemctl start httpd
sudo systemctl enable httpd
sudo systemctl status httpd --no-pager

5. Create Web Page
sudo mkdir -p /var/www/html
sudo chown -R ec2-user:ec2-user /var/www/html

echo "Hello Ayush 🚀 Your Apache web server is live on AWS EC2!" | sudo tee /var/www/html/index.html

6. Restart Apache
sudo systemctl restart httpd

7. Verify in Browser

Visit:

http://<EC2-PUBLIC-IP>


✔️ Should display:
Hello Ayush 🚀 Your Apache web server is live on AWS EC2!

🔹 GitHub Documentation
Project Setup
mkdir AWS-Apache-EC2-Project
cd AWS-Apache-EC2-Project

echo "*.pem" > .gitignore
echo "# AWS Apache EC2 Project" > README.md

Add Webpage
echo "Hello Ayush 🚀 Your Apache web server is live on AWS EC2!" > index.html

Initialize Git
git init
git add .
git commit -m "Initial commit - Apache EC2 project"

Connect GitHub Repo
git remote add origin https://github.com/aysharmaDevops/aws-ec2-apache-demo.git
git branch -M main
git push -u origin main



✅ Summary

Successfully:

Launched an EC2 instance

Installed Apache web server

Served a custom webpage

Pushed documentation + code to GitHub
