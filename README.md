# azure-terraform--bash

# 🔐 Terraform Azure Linux VM Lab

This project demonstrates the deployment of a secure Linux Virtual Machine on Microsoft Azure using Terraform. It includes complete infrastructure provisioning via infrastructure-as-code (IaC), dynamic SSH key generation, and tight network security using NSG rules.

---

## 📌 Lab Objectives

- Provision a Linux VM using Terraform with boot diagnostics
- Implement dynamic SSH key authentication via Azure API
- Secure access using inbound NSG rules for port 22 (SSH)
- Configure networking components like VNet, Subnet, and Public IP
- Output the VM's public IP for validation
- Practice clean DevSecOps-style provisioning


## 🧰 Included Terraform Scripts

- **main.tf**: Creates all core Azure resources — VM, VNet, NSG, NIC, etc.
- **variables.tf**: Defines configurable inputs like location and username
- **outputs.tf**: Displays VM’s public IP after deployment
- **providers.tf**: Declares provider requirements (Azure, Random)
- **ssh.tf**: Generates a unique SSH keypair using Azure API

## 🔐 Security Highlights

- Password authentication disabled by default
- SSH key generated dynamically at deploy time
- NSG enforces least privilege via inbound SSH rule
- Boot diagnostics logs stored in a secure Azure storage account

---

## 🚀 Deployment Steps

```bash
terraform init -upgrade
terraform plan -out main.tfplan
terraform apply main.tfplan
terraform output public_ip_address
```

✔️ Verify deployment via the Azure Portal under your selected Resource Group.

## 📎 Sample Output

172.191.149.66
```

## 🧠 Lessons Learned

This lab explores secure VM provisioning using API-driven SSH keys and proper Terraform modularity. It’s ideal for cloud engineers focused on DevSecOps and automated infrastructure builds.

## 🏷️ Tags

`terraform` `azure` `linux-vm` `iac` `network-security` `boot-diagnostics` `ssh-authentication` `cloud-infrastructure` `azure-cli` `devsecops`

## 🔗 Related Labs

- [Azure Resource Locks Lab](https://github.com/joshphillis/azure-resource-locks-lab)
- [Azure Kubernetes Bash Monitoring](https://github.com/joshphillis/azure-kubernetes---bash)
- [Event Hubs & Stream Analytics Lab](https://github.com/joshphillis/azure-event)

## 📣 Author

**Joshua Phillis**  
Multi-cloud engineer focused on secure infrastructure workflows, Terraform deployments, and DevSecOps pipelines.  


