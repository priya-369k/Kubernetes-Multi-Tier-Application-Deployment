# Kubernetes Multi-Tier Application Deployment

![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)

## Project Overview

Production-grade deployment of a multi-tier Java web application (V Profile) on Kubernetes cluster using **kops** for AWS infrastructure provisioning. This project demonstrates enterprise-level container orchestration, stateful application management, and cloud-native architecture implementation.

## Architecture

![Architecture Diagram](docs/images/architecture-diagram.png)

The application follows a microservices-based architecture with the following components:

- **Frontend/Load Balancer**: Nginx Ingress Controller with AWS Application Load Balancer
- **Application Server**: Apache Tomcat running Java application
- **Caching Layer**: Memcache for performance optimization
- **Message Queue**: RabbitMQ for asynchronous processing
- **Database**: MySQL with persistent EBS volume storage
  
## Technologies Used

### Infrastructure & Orchestration
- **Kubernetes 1.28+**: Container orchestration platform
- **kops 1.28+**: Kubernetes cluster provisioning tool
- **AWS EKS/EC2**: Cloud infrastructure provider
- **AWS EBS**: Persistent block storage

### Application Stack
- **Java/Tomcat 9**: Application runtime
- **MySQL 8.0**: Relational database
- **Memcache 1.6**: Distributed caching system
- **RabbitMQ 3.12**: Message broker

### DevOps Tools
- **Docker**: Containerization
- **kubectl**: Kubernetes CLI
- **Bash**: Automation scripting
- **Git**: Version control

## Prerequisites

Before deploying this project, ensure you have:

- AWS Account with appropriate IAM permissions
- AWS CLI configured (`aws configure`)
- kubectl installed (v1.28 or later)
- kops installed (v1.28 or later)
- Docker images from containerization project
- Domain name for ingress configuration (e.g., GoDaddy)
- Basic understanding of Kubernetes concepts

### Required IAM Permissions

AmazonEC2FullAccess

AmazonRoute53FullAccess

AmazonS3FullAccess

IAMFullAccess

AmazonVPCFullAccess
