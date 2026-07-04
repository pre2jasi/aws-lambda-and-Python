# aws-lambda-and-Python
Automate Security Compliance on AWS with Lambda &amp; Python

# 🛡️ Automated EC2 Security Compliance with AWS Lambda

The goal of this project is to write a Python script that automatically finds and terminates EC2 instances with SSH open to the world (`0.0.0.0/0`), then deploy it as an **AWS Lambda function** that runs automatically whenever a new EC2 instance is launched — powered by **Amazon EventBridge**.

---

## 🟢 Goal

Build a fully serverless, event-driven security automation pipeline that:

- Detects EC2 instances with security groups allowing unrestricted SSH access
- Automatically terminates non-compliant instances
- Triggers in real time on every new EC2 launch via EventBridge

---

## 🧱 Session Outline

### 1️⃣ Introduction & Project Overview
- Understand the security compliance use case and architecture overview

### 2️⃣ Development Environment Setup
- 🔹 Install Python
- 🔹 Install Boto3 and Ipykernel
- 🔹 Install Visual Studio Code
- 🔹 Install AWS CLI

### 3️⃣ VS Code Extensions
- 🔹 Install Python extension
- 🔹 Install Jupyter Notebook extension
- 🔹 Install JSON formatter extension

### 4️⃣ AWS Access and Version Control
- 🔹 Create IAM User with Programmatic Access
- 🔹 Run the `aws configure` command
- 🔹 Sign up for a free GitHub account
- 🔹 Create SSH key pairs
- 🔹 Add public SSH key to GitHub
- 🔹 Create and clone a Git repository

### 5️⃣ Write the Python Script
- 🔹 Write code in Jupyter Notebook step by step
- 🔹 Use Boto3 to query security group rules
- 🔹 Find groups with SSH open to the world (`0.0.0.0/0`)
- 🔹 Identify EC2 instances using those security groups
- 🔹 Terminate non-compliant instances
- 🔹 Convert notebook code to a Python script
- 🔹 Wrap code inside a Lambda handler function

### 6️⃣ Deploy the Lambda Function
- 🔹 Zip the Python script
- 🔹 Create an S3 bucket and upload the zip file
- 🔹 Create an IAM role for the Lambda function
- 🔹 Create the Lambda function
- 🔹 Upload Python code to Lambda
- 🔹 Update handler settings

### 7️⃣ Automate and Test
- 🔹 Add an EventBridge trigger for EC2 instance launches
- 🔹 Increase Lambda timeout to 30 seconds
- 🔹 Test the function manually
- 🔹 Launch EC2 instances with SSH open to the world
- 🔹 Watch Lambda detect and terminate non-compliant instances

### 8️⃣ Wrap-Up & Q&A
- Clean up AWS resources, assignment overview, and live Q&A

---

## 💡 Skills You'll Learn

- ✅ Python programming fundamentals
- ✅ Boto3 AWS SDK for Python
- ✅ Jupyter Notebook development workflow
- ✅ AWS Lambda function creation and deployment
- ✅ EventBridge triggers and event-driven automation
- ✅ IAM roles and policies for Lambda
- ✅ EC2 security group analysis
- ✅ S3 for Lambda code storage
- ✅ AWS CLI configuration and usage
- ✅ Git and GitHub version control
- ✅ Security compliance automation
- ✅ Serverless architecture patterns

---

## ☁️ AWS Services Covered

| Service | Purpose |
|---|---|
| **AWS Lambda** | Serverless compute for running the compliance script |
| **Amazon EC2** | Target resource being monitored and remediated |
| **Security Groups** | Source of the compliance rule being enforced |
| **Amazon EventBridge** | Event-driven trigger on EC2 launch |
| **IAM Roles & Policies** | Permissions for Lambda to inspect and terminate instances |
| **Amazon S3** | Storage for the Lambda deployment package |
| **AWS CLI** | Local configuration and AWS account access |

---

## 🔧 Development Tools Covered

`Python` • `Boto3` • `Jupyter Notebook` • `Visual Studio Code` • `Git` • `GitHub` • `AWS CLI`

---

## 🧠 Real-World Use Cases

- ✅ Automated security compliance enforcement
- ✅ Real-time threat detection and remediation
- ✅ Serverless security automation
- ✅ Event-driven infrastructure management
- ✅ DevSecOps automation pipelines
- ✅ Cloud security posture management
- ✅ Automated incident response
- ✅ Cost optimization through automated cleanup

---

## 🏗️ Architecture at a Glance

```
New EC2 Instance Launched
        │
        ▼
Amazon EventBridge (Rule: EC2 Instance State Change)
        │
        ▼
AWS Lambda Function
   ├── Boto3: Describe Security Groups
   ├── Check for 0.0.0.0/0 on port 22
   ├── Boto3: Describe Instances using flagged SG
   └── Boto3: Terminate non-compliant instance(s)
```

---

## 📄 License

This project is licensed under the MIT License.

```
MIT License

```
