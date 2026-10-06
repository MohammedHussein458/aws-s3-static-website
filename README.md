# AWS Cloud Architecture Project 1: Static Website Hosting on Amazon S3

![AWS S3](https://img.shields.io/badge/AWS-S3-orange?style=for-the-badge&logo=amazon-s3)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)
![Architecture](https://img.shields.io/badge/Architecture-Serverless-blue?style=for-the-badge)

## 📌 Project Overview
This project is part of a progressive hands-on Cloud Architecture learning path. The goal was to build, configure, and secure a static web application hosted on **Amazon Web Services (AWS)** using fundamental cloud storage and networking principles.

---

## 🏗️ Architecture Diagram & Components

```text
[ User / Browser ] 
        │
        │ HTTP Request (Port 80)
        ▼
┌─────────────────────────────────────────┐
│           Amazon S3 Bucket              │
│  ┌───────────────────────────────────┐  │
│  │ Static Website Hosting Endpoint    │  │
│  ├───────────────────────────────────┤  │
│  │  - index.html                     │  │
│  │  - Bucket Policy (Public Read)    │  │
│  └───────────────────────────────────┘  │
└─────────────────────────────────────────┘
