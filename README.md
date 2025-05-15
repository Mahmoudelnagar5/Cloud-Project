# 🌐 Azure Hub-and-Spoke Network Topology Deployment

This project demonstrates the deployment of a **Hub-and-Spoke** network topology on **Microsoft Azure**, designed to enhance security, scalability, and centralized control over network traffic. The solution includes virtual machines, virtual networks, network security groups, and web app deployment with monitoring and logging.

## 📁 Table of Contents

- [Overview](#overview-)
- [Architecture Diagram](#architecture-diagram-)
- [Project Goals](#project-goals-)
- [Step-by-Step Implementation](#step-by-step-implementation-)
- [Monitoring & Cost Estimation](#monitoring--cost-estimation-)
- [Tech Stack](#tech-stack-)
- [Documentation and Demo](#documentation-and-demo-)
- [Lessons Learned](#lessons-learned-)
- [References](#references-)

---

## Overview 📌

This project simulates a real-world **Hub-and-Spoke architecture** using Azure components. The central Hub VNet provides shared services, while Spoke VNets represent isolated environments (e.g., departments or applications). Connectivity, security, and monitoring are implemented for a complete cloud setup.

---

## Architecture Diagram 🧩

![Architecture Diagram](https://github.com/user-attachments/assets/e5cb908c-410e-4613-b03d-360ce293245c)

---

## Project Goals 🎯

- Create a Resource Group to manage all components.  
- Deploy one Hub VNet and three Spoke VNets.  
- Configure subnetting and VNet Peering.  
- Deploy a sample Web App using Azure App Services.  
- Implement NSGs to manage inbound traffic.  
- Enable Azure Monitor, Diagnostic Settings, and Log Analytics.  
- Deploy Web App using both Visual Studio Code and IIS.  
- Estimate cost and apply budget optimization.

---

## Step-by-Step Implementation 🛠️

### ✅ Step 1: Create Resource Group
- Resource Group Name: `HubSpoke-RG`  
- Region: West Europe  

### 🌐 Step 2: Create Hub and Spoke VNets
- `Hub-VNet` (10.0.0.0/16)  
- `Spoke1-VNet` (10.1.0.0/16)  
- `Spoke2-VNet` (10.2.0.0/16)  
- `Spoke3-VNet` (10.3.0.0/16)  

Each VNet has one subnet.

### 🔗 Step 3: VNet Peering
- Peer each Spoke with the Hub using VNet Peering (bi-directional).  
- Enable "Allow forwarded traffic" and "Use remote gateway" where applicable.

### 🌍 Step 4: Deploy Sample Web App
- Use Azure App Services (Node.js 18 LTS).  
- Hosting Plan: F1 (Free Tier).  
- Name: `hubwebapp123xyz`  
- Deploy via:  
  - Visual Studio Code  
  - IIS Deployment  

### 🔐 Step 5: Configure Network Security Groups (NSGs)
- Create NSG for each VNet.  
- Allow:  
  - HTTP (Port 80)  
  - HTTPS (Port 443)  
- Associate NSGs with respective subnets.

### 📊 Step 6: Enable Azure Monitor and Diagnostic Settings
- Create Log Analytics Workspace.  
- Enable Diagnostic Settings for:  
  - VNets  
  - Subnets  
  - App Services  
  - (Optional) VMs  
- Route logs to Azure Monitor and Log Analytics.

---

## Monitoring & Cost Estimation 💸

- Enabled Azure Monitor for all services.  
- Configured Metrics and Logs routing.  
- Estimated costs using:  
  - Azure Pricing Calculator  
  - Azure Cost Management + Budget Alerts  

💡 **Result:** Budget-friendly deployment using free tier and minimal usage.

---

## Tech Stack 🚀

- Microsoft Azure  
- Azure Virtual Network (VNet)  
- Network Security Groups (NSGs)  
- Azure App Services  
- Visual Studio Code & IIS  
- Azure Monitor & Log Analytics  
- Diagnostic Settings  
- Azure Cost Management  

---

## Documentation and Demo 📄

https://github.com/user-attachments/assets/613516b1-b381-4b79-99d1-1b56a6be449a

If you need the full project documentation in PDF format, feel free to contact me at:
📧 [Mahmoud Elnagar](mailto:elnagarm852@gmail.com)

---

## Lessons Learned 🧠

- Importance of centralized network management in Azure.  
- How to secure and monitor traffic using NSGs and monitoring tools.  
- Hands-on experience with VNet peering and diagnostics.

---

## References 📚

- [Microsoft Docs - Hub and Spoke](https://learn.microsoft.com/en-us/azure/architecture/reference-architectures/hybrid-networking/hub-spoke)  
- [Azure VNet Peering](https://learn.microsoft.com/en-us/azure/virtual-network/virtual-network-peering-overview)  
- [Azure Monitoring](https://learn.microsoft.com/en-us/azure/azure-monitor/overview)  
