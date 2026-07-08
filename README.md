<p align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&height=280&color=0:232F3E,50:1E90FF,100:56A8FF&text=AWS%20Static%20Website%20Hosting&fontSize=42&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Amazon%20S3%20|%20CloudFront%20|%20CodePipeline%20|%20CloudWatch%20|%20SNS&descAlignY=58"/>
</p>
<p align="center">
<img src="https://readme-typing-svg.demolab.com?font=Poppins&weight=700&size=24&duration=3500&pause=1200&color=1E90FF&center=true&vCenter=true&width=900&lines=AWS+Static+Website+Hosting;CI%2FCD+Pipeline+using+CodePipeline;CloudFront+%2B+S3+%2B+CloudWatch+%2B+SNS;Built+using+AWS+Best+Practices"/>
</p>
<div align="center">

# ☁️ AWS Static Website Hosting with CI/CD

### Secure Static Website Deployment using Amazon S3, CloudFront, IAM, CodePipeline & CloudWatch

<p align="center">

![AWS](https://img.shields.io/badge/AWS-Cloud-orange?style=for-the-badge&logo=amazonaws&logoColor=white)

![Amazon S3](https://img.shields.io/badge/Amazon-S3-red?style=for-the-badge&logo=amazons3&logoColor=white)

![CloudFront](https://img.shields.io/badge/Amazon-CloudFront-blue?style=for-the-badge&logo=amazonaws&logoColor=white)

![CodePipeline](https://img.shields.io/badge/AWS-CodePipeline-success?style=for-the-badge)

![CloudWatch](https://img.shields.io/badge/AWS-CloudWatch-yellow?style=for-the-badge)

![IAM](https://img.shields.io/badge/IAM-Security-important?style=for-the-badge)

![GitHub](https://img.shields.io/badge/GitHub-Repository-black?style=for-the-badge&logo=github)

</p>

![Visitors](https://komarev.com/ghpvc/?username=saisandeepgedela18&label=Repository%20Views&color=0e75b6&style=flat)

⭐ If you like this project, don't forget to Star the repository.

</div>

---

# 📖 Project Overview

This project demonstrates the deployment of a secure and scalable static website on **Amazon Web Services (AWS)** using modern **DevOps practices**.

The website is hosted on **Amazon S3**, distributed globally through **Amazon CloudFront**, secured using **Origin Access Control (OAC)**, continuously deployed using **AWS CodePipeline**, monitored with **Amazon CloudWatch**, and configured with secure access using **AWS Identity and Access Management (IAM)**.

The project was completed as part of an **AWS DevOps Internship**, focusing on cloud infrastructure, automation, security, monitoring, and CI/CD implementation.

---

# 🎯 Objectives

- Deploy a static website on AWS
- Configure secure Amazon S3 hosting
- Implement Amazon CloudFront CDN
- Secure the origin using Origin Access Control (OAC)
- Automate deployments using AWS CodePipeline
- Monitor infrastructure with CloudWatch
- Configure IAM users and least privilege access
- Implement monitoring alerts using Amazon SNS

---

# ✨ Key Features

✅ Static Website Hosting

✅ Global Content Delivery using CloudFront

✅ Origin Access Control (OAC)

✅ Continuous Integration & Continuous Deployment (CI/CD)

✅ GitHub Integration

✅ IAM Security

✅ CloudWatch Monitoring

✅ SNS Email Notifications

✅ Professional AWS Architecture

✅ Responsive Website Design

---

# 📑 Table of Contents

- Project Overview
- Objectives
- Features
- AWS Services Used
- Architecture
- Project Workflow
- Deployment Workflow
- Project Structure
- Screenshots
- CI/CD Pipeline
- CloudWatch Monitoring
- IAM Configuration
- Learning Outcomes
- Future Enhancements
- Contributors
- Author
- License

---
# ☁️ AWS Services Used

| AWS Service | Purpose |
|--------------|---------|
| **Amazon S3** | Hosts the static website files securely. |
| **Amazon CloudFront** | Delivers website content globally with low latency and Origin Access Control (OAC). |
| **AWS IAM** | Manages users, groups, roles, and permissions following the principle of least privilege. |
| **AWS CodePipeline** | Automates deployment from GitHub to Amazon S3. |
| **Amazon CloudWatch** | Monitors website performance and AWS resources. |
| **Amazon SNS** | Sends email notifications when CloudWatch alarms are triggered. |
| **GitHub** | Version control and source code management. |

---

# 🏗️ Project Architecture

```
                           +----------------------+
                           |     GitHub Repo      |
                           +----------+-----------+
                                      |
                                      |
                                      ▼
                          +-----------------------+
                          |   AWS CodePipeline    |
                          +----------+------------+
                                     |
                                     |
                                     ▼
                         +-------------------------+
                         |     Amazon S3 Bucket    |
                         |  (Static Website Files) |
                         +-----------+-------------+
                                     |
                     Origin Access Control (OAC)
                                     |
                                     ▼
                    +-------------------------------+
                    | Amazon CloudFront Distribution|
                    +---------------+---------------+
                                    |
                                    ▼
                           🌍 End Users / Browser

        +----------------------------------------------+
        |           Amazon CloudWatch                  |
        |  Dashboard • Metrics • Alarms • Monitoring   |
        +----------------------+-----------------------+
                               |
                               ▼
                       Amazon SNS Email Alerts
```

---

# 🔄 Project Workflow

```
Developer

↓

Push Source Code to GitHub Repository

↓

AWS CodePipeline Automatically Detects Changes

↓

Pipeline Deploys Files to Amazon S3

↓

Amazon CloudFront Fetches Updated Content

↓

Website Delivered Globally

↓

CloudWatch Monitors Infrastructure

↓

CloudWatch Alarm Triggered (if threshold exceeded)

↓

Amazon SNS Sends Email Notification
```

---

# 🔐 Security Implementation

The project follows AWS security best practices by implementing multiple security layers.

### ✅ IAM Security

- IAM Users created for each team member
- IAM Groups used for permission management
- Least Privilege Access implemented
- Separate permissions for:
  - Amazon S3
  - CloudFront
  - CloudWatch
  - CodePipeline

---

### ✅ Origin Access Control (OAC)

Instead of making the Amazon S3 bucket public, **Origin Access Control (OAC)** is configured.

Benefits:

- Prevents direct public access to S3
- Allows access only through CloudFront
- Improves website security
- Follows AWS recommended architecture

---

### ✅ Monitoring & Alerts

Amazon CloudWatch continuously monitors:

- Requests
- Error Rate
- Bucket Metrics
- Performance

CloudWatch Alarms trigger Amazon SNS notifications whenever configured thresholds are exceeded.

---

# 🚀 CI/CD Pipeline

The project uses **AWS CodePipeline** to automate deployments.

Pipeline Stages:

```
GitHub Repository

↓

Source Stage

↓

Deploy Stage

↓

Amazon S3

↓

CloudFront Distribution

↓

Live Website
```

### Benefits

- Automatic deployment
- Faster releases
- Reduced manual work
- Reliable updates
- Version control integration

---
# 📁 Project Structure

```text
AWS-Static-Website-Hosting-with-CI-CD/
│
├── website/
│   ├── index.html
│   ├── style.css
│   ├── script.js
│   └── Banner.jpeg
│
├── AWS/
│   ├── website-live.png
│   ├── cloudfront-distributions.png
│   ├── cloudfront-distribution-details.png
│   ├── cloudfront-origin.png
│   ├── cloudwatch-dashboard.png
│   ├── create-dashboard.png
│   ├── alarm-created.png
│   ├── alarm-configuration.png
│   ├── alarm-list.png
│   ├── codepipeline-success.png
│   ├── codepipeline-executions.png
│   ├── github-connection.png
│   ├── iam-user-groups.png
│   ├── member3-permissions.png
│   ├── member4-cloudwatch-permissions.png
│   ├── member5-codepipeline-permissions.png
│   └── sns-subscription-confirmed.png
│
├── documentation/
│
├── architecture/
│
├── assets/
│
└── README.md
```

---

# 🌐 Live Website

The website is successfully deployed using **Amazon S3** and securely distributed through **Amazon CloudFront**.

### Live URL

```
https://d3e31jbis4onz6.cloudfront.net
```
## 🌐 Live Demo

**CloudFront URL**

https://d3e31jbis4onz6.cloudfront.net

---

# 📸 Project Screenshots

## 🌍 Live Website

<p align="center">
<img src="website-live.png.jpeg" width="900">
</p>

---

## ☁️ Amazon CloudFront Distribution

<p align="center">
<img src="cloudfront-distributions.png.jpeg" width="900">
</p>

---

## 📄 CloudFront Distribution Details

<p align="center">
<img src="cloudfront-distribution-details.png.jpeg" width="900">
</p>

---

## 🔒 CloudFront Origin Access Control (OAC)

<p align="center">
<img src="cloudfront-origin.png.jpeg" width="900">
</p>

---

## 🔄 AWS CodePipeline

### Successful Deployment

<p align="center">
<img src="codepipeline-success.png.jpeg" width="900">
</p>

### Pipeline Executions

<p align="center">
<img src="codepipeline-executions.png.jpeg" width="900">
</p>

### GitHub Connection

<p align="center">
<img src="github-connection.png.jpeg" width="900">
</p>

### CodePipeline IAM Permissions

<p align="center">
<img src="member5-codepipeline-permissions.png.jpeg" width="900">
</p>

---

## 📊 Amazon CloudWatch Dashboard

<p align="center">
<img src="cloudwatch-dashboard.png.jpeg" width="900">
</p>

### Dashboard Creation

<p align="center">
<img src="create-dashboard.png.jpeg" width="900">
</p>

---

## 🚨 CloudWatch Alarm

### Alarm Configuration

<p align="center">
<img src="alarm-configuration.png.jpeg" width="900">
</p>

### Alarm Created

<p align="center">
<img src="alarm-created.png.jpeg" width="900">
</p>

### Alarm List

<p align="center">
<img src="alarm-list.png.jpeg" width="900">
</p>

---

## 📧 Amazon SNS Notification

<p align="center">
<img src="sns-subscription-confirmed.png.jpeg" width="900">
</p>

---

## 👥 IAM User Groups

<p align="center">
<img src="iam-user-groups.png.jpeg" width="900">
</p>

### CloudWatch Team Permissions

<p align="center">
<img src="member3-permissions.png.jpeg" width="900">
</p>

### CloudWatch IAM Policy

<p align="center">
<img src="member4-cloudwatch-permissions.png.jpeg" width="900">
</p>
# 📈 Project Outcome

✔ Successfully hosted a static website using Amazon S3.

✔ Configured Amazon CloudFront with Origin Access Control (OAC).

✔ Implemented Continuous Deployment using AWS CodePipeline.

✔ Connected GitHub Repository with AWS.

✔ Configured IAM Users and Groups following least privilege principles.

✔ Monitored infrastructure using Amazon CloudWatch.

✔ Configured CloudWatch Alarms and Amazon SNS notifications.

✔ Successfully validated website deployment through CloudFront.

---
# 👨‍💻 My Contribution

As **Member 3 (CloudFront Owner)**, I was responsible for the following tasks:

- Configured **Amazon CloudFront Distribution**
- Implemented **Origin Access Control (OAC)** for secure access to the S3 bucket
- Integrated Amazon S3 with CloudFront
- Configured the **Default Root Object** (`index.html`)
- Verified secure website accessibility through the CloudFront domain
- Tested website functionality after deployment
- Collected AWS implementation screenshots
- Organized the GitHub repository and project documentation

---

# 👥 Team Contributions

| Member | Responsibility |
|---------|----------------|
| **Member 1** | Amazon S3 Bucket Creation, Static Website Hosting & Bucket Policy |
| **Member 2** | IAM Users, Groups & Permission Management |
| **Sai Sandeep Gedela (Member 3)** | Amazon CloudFront Distribution, Origin Access Control (OAC), Website Testing & Repository Documentation |
| **Member 4** | Amazon CloudWatch Dashboard, Alarms & SNS Notifications |
| **Member 5** | GitHub Integration & AWS CodePipeline (CI/CD) |

---

# 🎓 Skills Gained

Throughout this project, I gained practical experience in:

- Amazon S3
- Amazon CloudFront
- Origin Access Control (OAC)
- AWS IAM
- AWS CodePipeline
- Amazon CloudWatch
- Amazon SNS
- GitHub
- CI/CD Pipeline
- Static Website Hosting
- AWS Security Best Practices
- Cloud Monitoring

---

# 📚 Learning Outcomes

This project helped me understand:

- Secure cloud infrastructure deployment
- Content delivery using CDN
- Continuous Integration & Continuous Deployment (CI/CD)
- AWS Identity & Access Management
- Monitoring cloud resources
- Infrastructure security using OAC
- Team collaboration using GitHub
- Practical AWS DevOps workflow

---

# 🚀 Future Enhancements

The project can be extended with:

- Custom Domain using Amazon Route 53
- HTTPS using AWS Certificate Manager (ACM)
- AWS WAF for web application security
- Infrastructure as Code using Terraform
- CloudFormation Templates
- GitHub Actions Integration
- AWS Lambda for serverless functionality
- Automated Testing before deployment

---

# 🏆 Project Highlights

- ✔ Secure Static Website Hosting
- ✔ Global Content Delivery
- ✔ Automated CI/CD Pipeline
- ✔ Cloud Monitoring & Alerts
- ✔ IAM Security Implementation
- ✔ GitHub Integration
- ✔ Professional DevOps Workflow

---

# 📜 Acknowledgement

This project was completed as part of an **AWS DevOps Internship**.

I sincerely thank all team members for their collaboration and support throughout the implementation of this project.

---

# 👤 Author

## Sai Sandeep Gedela

**B.Tech – Computer Science & Engineering**

**AWS DevOps Intern**

### Connect with Me

- **GitHub:** https://github.com/saisandeepgedela18
- **LinkedIn:** https://www.linkedin.com/in/sai-sandeep-gedela

---

# 📄 License

This project is developed for **educational and learning purposes** as part of an AWS DevOps Internship.

---

<div align="center">

## ⭐ If you found this project helpful, please consider giving it a Star!

### Thank you for visiting this repository! 🚀

Made with ❤️ by **Sai Sandeep Gedela**

</div>

