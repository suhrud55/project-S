**Full end-to-end **DevOps automation pipeline** **Integrating Terraform**, **Jenkins**, **ECR**, Kubernetes, and ** ArgoCD**


**Project Summary** — End-to-End DevOps Automation using Terraform, Jenkins, ECR, Kubernetes, and ArgoCD

This project demonstrates a complete CI/CD pipeline that automates the provisioning, containerization, and deployment of applications using modern DevOps tools and AWS infrastructure.

#### Infrastructure Automation (Terraform)

Used Terraform to provision cloud infrastructure on AWS, ensuring consistent, reusable, and version-controlled environments.

Created custom VPC network, public/private subnets, Internet Gateway, and Security Groups to host application resources securely.

Automated provisioning of RDS (MySQL) as the backend database.

Managed infrastructure state remotely using an S3 backend with state locking via DynamoDB.

#### Continuous Integration (Jenkins + Docker + ECR)

Configured Jenkins as the CI server to build, test, and package the application automatically.

Implemented Jenkins pipelines (Declarative or Scripted) for automation of build → Docker image creation → push to AWS Elastic Container Registry (ECR).

Integrated Webhooks to trigger builds automatically on every GitHub commit.

Used Dockerfiles to contain#erize both frontend and backend applications for consistent runtime environments.

### Continuous Deployment (Kubernetes + ArgoCD)

Defined Kubernetes YAML manifests for deployment, service, and ingress configurations.

Pulled application images directly from ECR and deployed them to a Kubernetes cluster (EKS).

Integrated ArgoCD for GitOps-based automation, enabling continuous deployment of application updates directly from GitHub.

Achieved zero-downtime deployments using Kubernetes rolling updates and health checks.

### Key Features

Fully automated pipeline from code commit → build → deploy → monitor

Infrastructure as Code (IaC) using Terraform

Containerization using Docker

CI/CD orchestration with Jenkins

Artifact management via AWS ECR

Deployment automation using ArgoCD + Kubernetes

Scalable and secure infrastructure using AWS VPC and RDS
