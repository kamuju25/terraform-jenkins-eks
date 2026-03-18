The goal of this setup is to -
# Automate application deployment to Kubernetes (EKS) using CI/CD and Infrastructure as Code.

What Each Tool Is Responsible for?

## GitHub

Purpose: Source code management
Stores your application code
Triggers Jenkins pipelines when changes happen

## Jenkins (CI/CD Engine)

Purpose: Automation
Builds your application (Java, etc.)
Runs tests
Creates artifacts (like Docker images)
Deploys to Kubernetes

## Terraform (Infrastructure as Code)

Purpose: Create infrastructure automatically
Creates AWS resources like:
EKS cluster
VPC, subnets
Security groups

## Amazon EKS (Kubernetes Cluster)

Purpose: Run your application
Managed Kubernetes by AWS
Hosts your containers (apps) --> This is where your app actually runs:

## Helm (Kubernetes Package Manager)

Purpose: Simplify deployments
Deploy apps to Kubernetes using templates
Manage versions and configurations easily
