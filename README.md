# AWS Solutions Architect Practice Projects

This repository contains hands-on architecture design projects aligned with the **AWS Certified Solutions Architect** exam. The solutions demonstrate my practical understanding of designing scalable, secure, and highly available systems on AWS.

Each project includes architecture diagrams and key design decisions based on real-world scenarios. The goal was not only to pass the exam but to **master AWS core services by applying them in complex, enterprise-level architectures**.

---

## 📌 Covered Concepts

- VPC design (CIDR planning, subnets, NAT, route tables)
- EC2 deployment in public/private subnets
- Layer 4 security controls (security groups, NACLs)
- IAM policies and identity-based access control
- Multi-AZ and Multi-region database architectures
- Load balancing and SSL offloading
- High availability and fault tolerance
- Cost optimization and serverless patterns
- Data durability and encryption at-rest/in-transit
- Hybrid cloud connectivity (on-premises whitelisting)

---

## ✅ Projects Overview

### **Project 1 – Multi-tier Web App with Secure Network Architecture**
Design a highly available and secure web application infrastructure.
- VPC with public/private subnets across 2 AZs
- EC2 instances for web & app tier
- Security at subnet and compute level (SG/NACL)
- Internet & programmatic access for admins/devs
- Global access optimization with Route 53 & CloudFront
- RDS multi-AZ with encryption and decoupling via SQS

### **Project 2 – Secure DB Access in Hybrid Architecture**
- Restrict DB access to app tier & corp data center via IP whitelisting
- EC2-based DB servers with NAT access for updates
- Prevent public internet exposure for database layer

### **Project 3 – Minimal Subnet Secure ELB Design**
- Two-tier architecture with SSL termination at ELB
- Web/App and RDS in private subnets
- Minimum subnets with high availability
- No internet access to backend, but outbound updates supported

### **Project 4 – Whitelist-based Web/App Tier**
- Application access allowed only from 2 on-prem IPs
- Highly available and scalable web/app tier
- Restrict inbound traffic to only whitelisted IPs

### **Project 5 – DB Tier with Reporting Isolation**
- Separate read-replica or data warehouse for reporting
- In-transit encryption enabled
- DB design prevents reporting load from affecting performance

### **Project 6 – Multi-region Low-Latency DB**
- Database replication with <1s lag across 2 regions
- RPO: 1s, RTO: <1min
- Elastic, scalable storage
- Support for complex queries & joins

### **Project 7 – Active-Active Global DB for E-Commerce**
- Active-active DB in `us-east-1` and `eu-west-1`
- Consistent low-latency reads/writes
- No DB management required (fully managed NoSQL)
- Flexible schema and scalable under heavy load

### **Project 8 – IAM Policy for EC2 Control via IP Range**
- IP-based condition in IAM policy for EC2 actions
- Allowed: `Start/Stop` only in `us-west-1`
- Deny all other EC2 actions
- Enforced IP restriction: `192.168.224.0/25`

### **Project 9 – Cost-Effective Durable File Recovery**
- Design using Amazon S3 + S3 Object Lock/Lifecycle
- Instant file recovery for 75 days
- Archived recovery within 48h up to 9 months
- Scalable and highly durable architecture

### **Project 10 – Secure Object Storage with Encryption Enforcement**
- S3 with default encryption
- Deny non-encrypted uploads via bucket policy
- Encryption key access restricted (KMS permissions)
- Designed for unpredictable access pattern & low cost

### **Project 11 – Tiered Object Storage with Quotas and Notifications**
- Free tier: 5GB, Paid tier: 100GB
- Track storage usage per user
- Notify users at 80% and 95% thresholds
- Designed for SaaS-like user-based storage management

---

## 🧰 Tools & Services Used

- **VPC, EC2, S3, RDS, IAM, KMS, Route 53, CloudFront**
- **NAT Gateway, Security Groups, NACLs**
- **Elastic Load Balancer (ALB/NLB)**
- **SQS for decoupling**
- **AWS Organizations and SCP (for advanced access control)**
- **CloudFormation (for infrastructure as code – in progress)**


---

## 🚀 Goal

This repository is part of my preparation for AWS Solutions Architect certification, but more importantly, a demonstration of **practical, production-grade design capabilities** in AWS.

Feel free to fork, star ⭐, or open an issue if you want to discuss the architecture of any of the projects!

---

## 🧑‍💼 Author

**Alireza Mokhtari**  
DevSecOps  
[LinkedIn](https://www.linkedin.com/in/alirezamokhtari82)

---

