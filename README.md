# 🚀 AWS EKS Cluster Provisioning using Terraform

## 📌 Overview

This project demonstrates how I provisioned a production-ready Amazon EKS cluster using Terraform, including networking, IAM roles, and managed node groups.

Unlike basic tutorials, this setup includes debugging real-world issues and applying proper DevOps workflows.

---

## 🛠️ Tech Stack

* Terraform
* AWS EKS
* VPC
* IAM
* Kubernetes

---

## ⚙️ Features

* Custom VPC with public & private subnets
* NAT Gateway for private networking
* Managed EKS cluster (Kubernetes 1.29)
* Node group with autoscaling
* IRSA enabled (OIDC provider)
* Secure networking with security groups

---

## 🚀 Deployment Steps

### 1. Configure AWS

```bash
aws configure
```

---

### 2. Initialize Terraform

```bash
terraform init
```

---

### 3. Plan Infrastructure

```bash
terraform plan
```

---

### 4. Apply Configuration

```bash
terraform apply
```

---

## 🔗 Connect to Cluster

```bash
aws eks update-kubeconfig --name <cluster-name> --region us-west-2
kubectl get nodes
```

---

## ⚠️ Challenges & Fixes

### ❌ Unsupported Kubernetes Version

* Issue: EKS rejected version 1.27
* Fix: Updated to 1.29

### ❌ Provider Compatibility Issue

* Issue: Unsupported block errors
* Fix: Aligned AWS provider with module version

### ❌ Git Hygiene Issues

* Removed `.terraform.lock.hcl`
* Prevented `.tfstate` from being committed

---

## 📊 Result

* EKS cluster successfully provisioned
* Nodes running and accessible
* Clean Git workflow implemented

---

## 🚀 Future Improvements

* Remote backend (S3 + DynamoDB)
* CI/CD pipeline (GitHub Actions)
* Deploy applications to EKS
* ALB Ingress Controller setup

---

## 👤 Author

Bharath Ranganathan
