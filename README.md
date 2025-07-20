# Benchmarking CloudNativePG in a Confidential Multi-Cloud

This repository accompanies the thesis _"Benchmarking CloudNativePG in a Confidential Multi-Cloud"_ (Fiete Scheel, Jan-Frederik Felsch, July 2025), which investigates the feasibility and performance of running PostgreSQL in a geo-distributed, Kubernetes-based multi-cloud environment using Confidential Virtual Machines (cVMs).

## Project Overview

The project sets up two Kubernetes clusters:

- One using **Confidential VMs** with AMD SEV-SNP technology
- One using **regular VMs**

Both clusters are distributed across:

- 🇺🇸 `us-central1`
- 🇪🇺 `europe-north1`
- 🇦🇸 `asia-east1`

The goal is to benchmark and compare performance, security, and scalability using the [CloudNativePG](https://cloudnative-pg.io/) operator for PostgComponents

- **Kubernetes** clusters via [RKE2](https://docs.rke2.io/)
- **PostgreSQL** via CloudNativePG Operator
- **Confidential Computing** using AMD SEV-SNP on Google Cloud
- **WireGuard VPN** for secure inter-node communication
- **Vault + vHSM** for remote attestation & secret management
- **OpenEBS** for persistent encrypted storage (Confidential VMs only)
