# linux-first-mini-project

# Mini Project: AWS EC2 Ubuntu Server Setup

This project demonstrates how to set up an AWS account, provision an EC2 instance with Ubuntu, connect to the instance, and manage software using the terminal.

---

## 🔧 1. AWS Account Setup and Ubuntu EC2 Provisioning

### Step 1: Create an AWS Account
- Visit [https://aws.amazon.com/](https://aws.amazon.com/)
- Signed up for a new account using my email and billing info.
- Complete identity verification and security setup.

### Step 2: Launch an EC2 Instance
- Navigated to **EC2 Dashboard**.
- Click **Launch Instance**.
- Choose a name for your instance.
- Select the **Ubuntu** AMI (Amazon Machine Image).
  ![](https://github.com/adaezeokoduwa/linux-first-mini-project/blob/main/images/ubuntu-start.png?raw=true)
- Choose an instance type (e.g., `t2.micro` for Free Tier).
- Create a new key pair (or use an existing one).
- Set network settings to allow **SSH** access (port 22).
- Click **Launch Instance**.
![](https://github.com/adaezeokoduwa/linux-first-mini-project/blob/main/images/lunched-instance.png?raw=true)

![](https://github.com/adaezeokoduwa/linux-first-mini-project/blob/main/images/instance-running.png?raw=true)
![](https://github.com/adaezeokoduwa/linux-first-mini-project/blob/main/images/instance-running2.png?raw=true)
---

## 🔌 2. Connecting to Your EC2 Instance

### Step 1: Locate Your Key Pair
- Ensure your `.pem` key is downloaded and saved securely.

### Step 2: Connect via SSH
-Open your terminal.

Use the command format below to connect

``
ssh -i your-key-name.pem ubuntu@your-ec2-public-ip
``

![](https://github.com/adaezeokoduwa/linux-first-mini-project/blob/main/images/ubuntu-connection.png?raw=true)

## ⚙️ 3. Installing, Updating, and Removing Software
### Step 1: Update System Packages
After SSHing into your server, run:
``
sudo apt update && sudo apt upgrade -y
``
![](https://github.com/adaezeokoduwa/linux-first-mini-project/blob/main/images/updating-ubuntu-app.png?raw=true)

![](https://github.com/adaezeokoduwa/linux-first-mini-project/blob/main/images/app-upgrade.png?raw=true)
### Step 2: Install Software
Example: Install Nginx web server:
``
sudo apt install nginx -y
``

### Step 3: Start and Enable the Service
``
sudo systemctl start nginx
sudo systemctl enable nginx
``

### Step 4: Remove Unwanted Software
``
sudo apt remove nginx -y
``
