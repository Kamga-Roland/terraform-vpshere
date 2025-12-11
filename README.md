# Terraform vSphere VM Automation with Packer

This repository contains Infrastructure as Code (IaC) for automating virtual machine provisioning on VMware vSphere using **Terraform** and **Packer**.  
It enables consistent VM builds, rapid deployment, and simplified lifecycle management.

---

## 🚀 Features
- Automated VM creation on vSphere with Terraform
- Golden image building with Packer
- Configurable CPU, memory, disk, and network settings
- Support for cloning from templates
- Easy customization via variables

---

## 📦 Prerequisites
- [Terraform](https://developer.hashicorp.com/terraform/downloads) >= 1.0
- [Packer](https://developer.hashicorp.com/packer/downloads)
- VMware vSphere environment (vCenter + ESXi)
- vSphere credentials with sufficient permissions
- Access to a datastore and network in vSphere

---

## ⚙️ Setup

1. **Clone the repo**
   ```bash
   git clone https://github.com/your-org/terraform-vsphere-vm-automation.git
   cd terraform-vsphere-vm-automation
vsphere_user     = "administrator@vsphere.local"
vsphere_password = "yourpassword"
vsphere_server   = "vcenter.example.com"

2. **Configure variables
Create or edit terraform.tfvars:**
datacenter_name  = "Datacenter"
cluster_name     = "Cluster"
datastore_name   = "Datastore"
network_name     = "VM Network"
ubuntu_name      = "ubuntu-template"

3. **Build base image with Packer**
   ```bash packer build packer/ubuntu.json

5. **Initialize Terraform**
   ```bash terraform init

6. **Validate configuration**
   ```bash terraform validate

7. **Preview changes**
    ```bash terraform plan

8. **Apply configuration**
    ```bash terraform apply

9. **Destroy resources (optional)**
    ```bash terraform destroy

