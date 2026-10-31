
The infrastructure is engineered with multiple layers of network and access security:
* **Virtual Network (VNet) & Subnetting:** Configu# My First Azure Project
# Azure Windows Virtual Machine Deployment & Secure RDP Infrastructure

## 📌 Project Overview
This repository contains the architecture, documentation, and implementation steps for deploying a highly secure Windows Virtual Machine (VM) on Microsoft Azure. The primary focus of this project is establishing a robust cloud infrastructure featuring network isolation, secure remote endpoints via Remote Desktop Protocol (RDP), automated daily data protection, and high-availability setups.

## 🏗️ Architecture Componentsred a dedicated Azure VNet with custom address spaces and isolated public/private subnets to control traffic boundaries.
* **Network Security Groups (NSGs):** Implemented strict inbound and outbound firewall security rules, restricting RDP access solely to authorized source endpoints to minimize the network attack surface.
* **Azure Compute:** Provisioned a Windows Server Virtual Machine optimized for stable and scalable cloud compute workloads.
* **Azure Storage & Backup Center:** Integrated Azure Blob Storage rules for static asset management and deployed Azure Backup Center to enforce systemic, daily automated snapshots for data disks and disaster recovery.



## 🛠️ Step-by-Step Implementation Guide

### Phase 1: Networking & Security Foundation
1. **Create Virtual Network:** Provisioned an Azure VNet (`VNet-Prod-01`) within the resource group, assigning a secure IP address range.
2. **Subnet Delegation:** Divided the network into frontend (public-facing) and backend (private) subnets to enforce strict tier isolation.
3. **Configure NSG Rules:** Created a Network Security Group (`NSG-Secure-RDP`), explicitly blocking all public traffic by default and allowing inbound RDP (Port 3389) traffic strictly from specified IP endpoints.

### Phase 2: Compute Provisioning & Connectivity
1. **VM Deployment:** Deployed a standard Windows Server VM, attaching it directly to the designated secure subnet.
2. **Storage Optimization:** Attached data disks and set up secure Azure Blob Storage containers for structured asset storage.
3. **RDP Configuration:** Securely established remote endpoints and verified seamless connection testing via Remote Desktop Protocol using public/private network rules.

### Phase 3: Automation & Business Continuity
1. **Backup Enrolment:** Registered the active production VM under the Azure Backup Vault.
2. **Snapshot Scheduling:** Defined custom daily snapshot policies to enforce systemic backup configurations, ensuring minimal downtime and robust disaster recovery capabilities.
3. **Recovery Verification:** Regularly tested cloud recovery points to validate successful system restore options.

---

## 💻 Tech Stack & Tools Used
* **Cloud Provider:** Microsoft Azure (Compute, Storage, Networking, IAM, Backup Center)
* **Operating System:** Windows Server / Remote Desktop Client
* **Version Control:** Git & GitHub

---

## 🚀 Key Takeaways & Impact
* **Zero Trust Security:** Effectively reduced corporate network exposure by securing RDP endpoints and applying strict Network Security Groups.
* **Automated Reliability:** Scaled infrastructure operations from manual tracking to an automated daily backup lifecycle, preventing operational data loss.
* **Hands-On Cloud Expertise:** Gained fundamental experience handling production-grade cloud resource configuration, IAM roles, and network architecture logic.
