# Azure Cloud Foundation Project

## Overview
This project demonstrates the foundational setup of a public cloud environment using the Microsoft Azure Free Tier. It covers cloud governance infrastructure, Role-Based Access Control (RBAC), regional architecture selection, and cloud cost management safeguards.

## Infrastructure Architecture & Governance
- **Subscription Type:** Azure Free Tier
- **Resource Group Name:** `rg-cloud-project-prod`
- **Deployment Region:** South Africa North (Johannesburg)

### Regional Selection Rationale
The **South Africa North** region was selected to host all resources. For users located in West Africa, leveraging a data center on the African continent drastically reduces round-trip network latency compared to routing traffic to European data centers, resulting in faster data retrieval and better overall application performance.

## Deployed Resource & The Shared Responsibility Model
For Task 6, a **Microsoft Azure Storage Account** was deployed. Because this is a **Platform as a Service (PaaS)** model, the boundaries of security and maintenance shift significantly compared to traditional infrastructure:

1. **Microsoft's Responsibility:** As the cloud provider, Microsoft fully manages the underlying physical infrastructure, data center security, host servers, hypervisors, physical storage disks, operating system patching, and the core storage runtime.
2. **My (The Customer's) Responsibility:** I am entirely responsible for the data stored within the account and its configuration boundaries. This includes implementing Identity and Access Management (IAM/RBAC) to control who can access the data, rotating storage access keys, enabling forced HTTPS encryption for data in transit, configuring network firewalls (if required), and ensuring data isn't accidentally exposed to the public internet.

## Project Deliverables
All structural screenshots confirming the active dashboard, resource group configuration, deployment success, and cost monitoring safeguards can be found in the `/screenshots` directory of this repository.
