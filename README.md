
# 🚀 Simple VPC Design on AWS

## 📌 Project Overview

This project demonstrates the creation of a **Simple Virtual Private Cloud (VPC)** in Amazon Web Services (AWS). It includes a custom VPC, public and private subnets, an Internet Gateway, route tables, security groups, and an EC2 instance deployed in the public subnet.

The project was completed as part of an **AWS Cloud Internship** to understand the fundamentals of AWS networking and cloud infrastructure.

---

## 🏗️ Architecture

```
                    Internet
                        │
                Internet Gateway
                        │
        ┌────────────────────────────┐
        │        intern-vpc          │
        │       10.0.0.0/16          │
        │                            │
        │ ┌────────────┐             │
        │ │ Public     │             │
        │ │ Subnet     │             │
        │ │10.0.1.0/24 │             │
        │ └─────┬──────┘             │
        │       │                    │
        │   intern-ec2               │
        │   (EC2 Instance)           │
        │                            │
        │ ┌────────────┐             │
        │ │ Private    │             │
        │ │ Subnet     │             │
        │ │10.0.2.0/24 │             │
        │ └────────────┘             │
        └────────────────────────────┘
```

---

## 🎯 Objective

- Create a custom Virtual Private Cloud (VPC).
- Configure public and private subnets.
- Enable internet connectivity using an Internet Gateway.
- Launch an EC2 instance in the public subnet.
- Configure route tables and security groups.
- Understand AWS networking fundamentals.

---

## 🛠 AWS Services Used

- Amazon VPC
- Amazon EC2
- Internet Gateway
- Route Tables
- Security Groups

---

## 📋 Project Configuration

| Resource | Configuration |
|----------|---------------|
| VPC Name | intern-vpc |
| VPC CIDR | 10.0.0.0/16 |
| Public Subnet | 10.0.1.0/24 |
| Private Subnet | 10.0.2.0/24 |
| Internet Gateway | Attached |
| Route Table | Public Route Table |
| EC2 Name | intern-ec2 |
| Instance Type | t2.micro |
| Operating System | Amazon Linux 2 |
| Security Group | SSH (22), HTTP (80), HTTPS (443) |

---

## 📂 Project Steps

### Step 1
Create a custom VPC with CIDR block **10.0.0.0/16**.

### Step 2
Create:

- Public Subnet (10.0.1.0/24)
- Private Subnet (10.0.2.0/24)

### Step 3
Create and attach an Internet Gateway to the VPC.

### Step 4
Create a Public Route Table and add:

| Destination | Target |
|-------------|--------|
| 0.0.0.0/0 | Internet Gateway |

Associate it with the Public Subnet.

### Step 5
Enable **Auto Assign Public IPv4 Address** for the Public Subnet.

### Step 6
Launch an EC2 instance (**intern-ec2**) in the Public Subnet.

### Step 7
Configure the Security Group:

- SSH (22)
- HTTP (80)
- HTTPS (443)

### Step 8
Connect to the EC2 instance using PuTTY or SSH.

### Step 9
Verify internet connectivity:

```bash
ping google.com
```

---

## 📁 Repository Structure

```
Simple-VPC-Design/
│
├── README.md
├── architecture-diagram.png
├── screenshots/
│   ├── 01-vpc.png
│   ├── 02-subnets.png
│   ├── 03-route-table.png
│   ├── 04-internet-gateway.png
│   ├── 05-security-group.png
│   ├── 06-ec2-instance.png
│   └── 07-ssh-connected.png
└── Project_Report.pdf
```

---

## 📸 Screenshots

Add the following screenshots:

- VPC
- Public & Private Subnets
- Internet Gateway
- Route Table
- Security Group
- EC2 Instance
- SSH Connection
- Ping Test

---

## ✅ Expected Output

- Custom VPC successfully created.
- Public and private subnets configured.
- Internet Gateway attached.
- Route table configured.
- EC2 instance launched in the public subnet.
- SSH connection established.
- Internet connectivity verified.

---

## 🎓 Learning Outcomes

- AWS VPC Fundamentals
- IP Addressing and CIDR Blocks
- Public and Private Subnets
- Internet Gateway Configuration
- Route Table Association
- EC2 Deployment
- Security Group Configuration
- Basic Cloud Networking

---

## 🔮 Future Enhancements

- Add a NAT Gateway for private subnet internet access.
- Deploy a web server on the EC2 instance.
- Configure Load Balancer.
- Launch multiple EC2 instances.
- Integrate Auto Scaling.
- Monitor infrastructure using Amazon CloudWatch.

---

## 👨‍💻 Author

**Shivam Akash**

AWS Cloud Internship Project
