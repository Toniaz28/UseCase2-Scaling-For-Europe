# 📘 Use Case 2: Scaling NovaTech for Europe

## Platform Explorers Cohort 2 — Azure Administration (AZ-104) Track

---

# 📌 Project Overview

This project extends NovaTech Solutions’ cloud infrastructure from the US to Europe using Microsoft Azure.

The goal is to build a secure, scalable, multi-region architecture that includes networking, compute, security, monitoring, and cost management.

---

# 🌍 Scenario

NovaTech Solutions has an existing Azure environment in **East US** and is expanding to **West Europe** for 50 new employees.

The European environment must:

- Connect securely to US resources
- Host local compute workloads
- Support load balancing
- Secure secrets using Key Vault
- Monitor performance and costs

---


This project extends NovaTech Solutions’ existing Azure infrastructure from the East US region into West Europe. The goal was to design and implement a secure, scalable, and production-like multi-region cloud architecture using Microsoft Azure.

The environment includes networking, compute, security, monitoring, and cost management services configured across both regions to simulate real-world enterprise cloud expansion.

The project demonstrates how enterprise workloads can be securely extended across regions while maintaining observability, scalability, and cost control.

---

## ⚠️ Task 7 – Key Vault Access Issue

During Task 7, I was unable to retrieve the stored secret from Azure Key Vault using Azure CLI due to insufficient permissions.

Despite attempting to access the secret using the required command, access was denied because my account did not have the necessary Key Vault permissions (RBAC role or Access Policy not assigned).

This highlights the importance of proper role-based access control (RBAC) or access policy configuration when working with Azure Key Vault in production environments.



---

# 🏗️ Architecture Summary

The solution includes:

- East US VNet (10.0.0.0/16)
- West Europe VNet (172.16.0.0/16)
- VNet Peering (bidirectional)
- Private DNS Zone for internal resolution
- Load Balancer for web tier traffic
- Azure Container Instance (Nginx API service)
- Key Vault for secrets management
- Log Analytics Workspace for monitoring
- Azure Monitor Alerts (CPU & Disk)
- Azure Budget ($30 limit)

---

## 📁 Project Structure

```text
UseCase2-Scaling-For-Europe/
├── screenshots/
│   ├── 01-europe-resource-group.png
│   ├── 02-europe-vnet.png
│   ├── 03a-peering-eastus.png
│   ├── 03b-peering-westeurope.png
│   ├── 04-dns-zone.png
│   ├── 05a-lb-overview.png
│   ├── 05b-lb-backend-pool.png
│   ├── 05c-lb-health-probe.png
│   ├── 05d-lb-browser-test.png
│   ├── 06-aci-overview.png
│   ├── 07-keyvault-secret.png
│   ├── 08-log-analytics.png
│   ├── 09-monitor-alert.png
│   ├── 10-budget.png
│   ├── 11a-advisor-eastus.png
│   ├── 11b-advisor-westeurope.png
│   └── 12-cleanup-confirmation.png
├── thought-process.md
├── challenge-answers.md
└── README.md
```



