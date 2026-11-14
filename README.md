# Devops-practice-lab

This repository is a hands-on, chapter‑based guide to building and deploying cloud-native applications
using Terraform, Kubernetes, Flux, and related tools. Each numbered folder represents a self‑contained
"chapter" focused on a particular area of the development‑to‑operations lifecycle.

---

## Chapters Overview

1. **Terraform** (`1-terraform/`)
   - Learn the fundamentals of Terraform by solving a networking problem with AWS Lambda.
   - Focuses on private networking, VPCs and internet access from isolated functions.

2. **Kubernetes Cluster** (`2-kubernetes-cluster/`)
   - Create and manage an Amazon EKS (or local Kind/Minikube) cluster with Terraform.
   - Install Flux v2 in the cluster to bootstrap the continuous-deployment flow.

3. **Continuous Deployment** (`3-continuous-deployment/`)
   - Use FluxCD and Helm to continuously deliver workloads into the cluster.
   - Build Docker images, publish them to a registry, and deploy with Helm charts.
   - Exercise includes NATS messaging, producer/consumer services, and Benthos.

4. **Telemetry** (`4-telemetry/`)
   - Add observability via metrics, logs and tracing (OpenTelemetry, Prometheus, Grafana, Jaeger).
   - Instrument services and visualize metrics/traces in dashboards.

5. **Secrets** (`5-secrets/`)
   - Manage sensitive data for applications using Vault (or sealed‑secrets) instead of plaintext.
   - Integrate secrets into Kubernetes workloads securely.

6. **Continuous Integration** (`6-continuous-integration/`)
   - Configure GitHub Actions pipelines to validate infrastructure on each push.
   - Run Terraform/Helm tests and publish charts based on tags.

7. **Service Mesh** (`7-service-mesh/`)
   - (TBD) Explore service mesh concepts, policies and tooling (e.g. Cilium, Istio) in Kubernetes.

---

## Getting Started

1. Clone this repository and browse the chapter directories.
2. Follow the README in each chapter for exercises, suggested roadmaps, and references.
3. You can work sequentially through the chapters or focus on particular areas of interest.
4. Many chapters rely on an AWS account; configure your CLI credentials before running Terraform.
5. Use `kubectl` and `k9s` to inspect clusters; `terraform` to provision resources; and `flux` to manage deployments.

> 💡 The structure is intentionally minimal to encourage experimentation. Feel free to adapt,
> extend or repurpose the examples for your own learning path.

---


## Prerequisites

Before starting the hands-on exercises, make sure your
development environment is configured with the appropriate tools.

| Tool | Purpose |
|------|---------|
| Git | Clone the repository and manage source code |
| Terraform | Provision and manage infrastructure as code |
| AWS CLI | Configure AWS credentials and access AWS services |
| Docker | Build and run containerized applications |
| kubectl | Manage Kubernetes clusters and workloads |
| Helm | Package and deploy Kubernetes applications |
| Flux CLI | Manage GitOps-based continuous deployment |
| k9s (optional) | Explore and monitor Kubernetes resources |

> **Note:** Not every chapter requires every tool.
> Check the individual chapter README for specific requirements.

---

## Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/Tendor292527/devops-practice-lab.git
cd devops-practice-lab
```

### 2. Explore the Chapters

```bash
ls
cd 1-terraform
```

Read the chapter-specific README before running any commands.

### 3. Verify Your Development Tools

```bash
git --version
terraform version
aws --version
docker --version
kubectl version --client
helm version
flux --version
```

Install any missing tools required by the chapter you plan to complete.

### 4. Configure AWS Access (When Required)

```bash
aws configure
aws sts get-caller-identity
```

Use credentials with permissions appropriate to the exercise.

Some cloud resources may incur charges, so review Terraform
plans and clean up resources after completing exercises.

---

## Contributing

Contributions, documentation improvements, and bug fixes
are welcome.

1. Create a new branch from the default branch.
2. Make a focused improvement to the relevant chapter or documentation.
3. Test or validate your changes when applicable.
4. Commit your changes with a descriptive message.
5. Open a pull request explaining what changed and why.

For documentation contributions, verify that commands,
file paths, and Markdown links are accurate.

---
  
## Resources

- `cr.yaml` contains repository metadata used by automated tooling.
- Each chapter has its own `README.md` with detailed instructions and references.

---

Happy learning! 🚀
