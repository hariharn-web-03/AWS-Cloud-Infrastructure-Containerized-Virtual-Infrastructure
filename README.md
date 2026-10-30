# AWS Cloud Infrastructure & Containerized Virtual Infrastructure ☁️🐳

A robust cloud engineering and containerization project demonstrating the deployment of a secure Multi-Tier AWS Virtual Private Cloud (VPC) architecture integrated with containerized microservices (WordPress & MySQL via Docker).

---

## 📋 Table of Contents
- [Architecture Overview](#-architecture-overview)
- [Core AWS Components Implemented](#-core-aws-components-implemented)
- [Three-Tier Containerized Deployment](#-three-tier-containerized-deployment)
- [Storage & Backup Management](#-storage--backup-management)

---

## 🏗️ Architecture Overview
* **Virtual Private Cloud (VPC)**: Configured with customized IPv4 CIDR blocks (`192.168.0.0/16`) spanning public and private subnets[cite: 242, 244, 245].
* **Internet Connectivity**: Attached Internet Gateways (IGW) and configured public/private route tables for secure traffic routing[cite: 246, 247].
* **Security Groups & Network ACLs**: Implemented strict inbound/outbound firewall rules limiting access to HTTP/HTTPS, SSH, and database ports (`MySQL 3306`)[cite: 249, 255].

---

## ⚙️ Core AWS Components Implemented
1. **EC2 Instance Provisioning**: Launched and configured multi-OS virtual servers (`Amazon Linux 2023`, `Red Hat Enterprise Linux`, `Ubuntu`, and `Windows Server`) with secure key pair authentication (`.pem`)[cite: 230, 232, 235].
2. **Elastic IP & Elastic Block Store (EBS)**: Allocated static IPs and attached scalable EBS volumes (`xfs` formatted and mounted) with automated snapshot policies[cite: 253, 264, 266].
3. **Amazon S3**: Provisioned general-purpose S3 buckets for secure object storage and asset management[cite: 267].

---

## 🐳 Three-Tier Architecture with Containers
* **Database Tier**: Deployed a persistent MySQL container instance[cite: 270].
* **Application Tier**: Deployed an official WordPress container linked directly to the database backend[cite: 273].
* **Verification**: Validated database connectivity, user provisioning, and web dashboard configuration[cite: 276].
