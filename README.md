# AWS 3-Tier Architecture Deployment Using Terraform & GitHub Actions

## Project Workflow

```text
Developer Pushes Code to GitHub
                │
                ▼
        GitHub Actions Triggered
                │
                ▼
     Terraform Infrastructure Provisioning
                │
                ▼
        AWS Resources Created
    (VPC, Subnets, EC2, NAT, SG)
                │
                ▼
      Frontend & Backend Deployment
                │
                ▼
      Application Connected to Database
                │
                ▼
     Automatic Deployment Completed
```

---

# Infrastructure Workflow

```text
                Internet
                    │
        ┌─────────────────────┐
        │ Internet Gateway    │
        └─────────────────────┘
                    │
        ┌─────────────────────┐
        │ Public Subnet       │
        │ Bastion Host        │
        │ Frontend Server     │
        └─────────────────────┘
                    │
              NAT Gateway
                    │
        ┌─────────────────────┐
        │ Private Subnet      │
        │ Backend Server      │
        └─────────────────────┘
                    │
        ┌─────────────────────┐
        │ Database Subnet     │
        │ MySQL / RDS         │
        └─────────────────────┘
```

---

# CI/CD Workflow

```text
GitHub Repository
        │
        ▼
GitHub Actions Workflow
        │
        ├── Install Dependencies
        ├── Build Frontend
        ├── Build Backend
        ├── SSH into EC2
        ├── Deploy Application
        └── Restart Services
                │
                ▼
        AWS EC2 Instances Updated
```

---

# Screenshots

## Terraform Apply
<img width="100%" alt="terraform-apply" src="./screenshots/terraformInit.png">
<img width="100%" alt="terraform-apply" src="./screenshots/terraformPlan.png">
<img width="100%" alt="terraform-apply" src="./screenshots/terraformApply1.png">
<img width="100%" alt="terraform-apply" src="./screenshots/terraformApply2.png">
-----

## AWS VPC
![VPC](./screenshots/vpc1.png)

---

## Public and Private Subnets
![Subnets](./screenshots/subnets.png)

---

## EC2 Instance
![EC2 Instances](./screenshots/Instances.png)

---

## Security Groups
![Security Groups](./screenshots/securitygroups.png)

---

## Route Tables
![Route Tables](./screenshots/routetables.png)

---

## Internet Gateway
![Internet Gateway](./screenshots/internetgateway.png)

---

## NAT Gateway
![NAT Gateway](./screenshots/natgateway.png)

---

## Elastic IP
![Elastic IP](./screenshots/elasticIp.png)

## GitHub Actions Workflow

<img width="100%" alt="github-actions" src="screenshots/github-actions.png">

---

## Successful CI/CD Deployment

<img width="100%" alt="deployment-success" src="screenshots/deployment-success.png">

---

## Frontend Application

<img width="100%" alt="frontend" src="screenshots/frontend.png">

---

## Backend API Response

<img width="100%" alt="backend" src="screenshots/backend.png">

---

## Database Connection

<img width="100%" alt="database" src="screenshots/database.png">

---

## Terraform Code

<img width="100%" alt="architecture" src="screenshots/architecture.png">

---