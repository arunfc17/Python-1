# DevOps Showcase

Small, opinionated end-to-end DevOps demo project showing:
- Node.js sample microservice with Prometheus metrics
- Docker multi-stage build and best practices
- Helm chart for Kubernetes deployment
- Terraform skeleton for cloud infra (AWS/EKS example)
- GitHub Actions:
  - CI (lint, test, build image, security scans)
  - Terraform plan
  - CD deploy to cluster
- Security: hadolint, Trivy, eslint
- Observability: Prometheus metrics endpoint

Quickstart (local)
1. Build and run locally:
   - cd app
   - npm ci
   - npm start
   - Visit http://localhost:3000/ and http://localhost:3000/metrics

2. Build Docker image:
   - docker build -t devops-showcase:local .

3. Helm deploy to cluster:
   - helm upgrade --install devops-showcase ./helm -n devops --create-namespace

CI / CD
- The GitHub Actions workflows build/test and push images to GitHub Container Registry (ghcr.io) and run Terraform plan.
- Configure required GitHub secrets listed in README before enabling workflows.

Project layout
- app/: Node.js application, tests, Dockerfile
- helm/: Helm chart for deployment
- infra/: Terraform scaffold for provisioning cloud infra (modules/eks)
- .github/workflows/: CI, TF plan and CD workflows
- scripts/: convenience scripts for local bootstrap and cleanup

License: MIT
