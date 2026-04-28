# 🌐 Terraform Multi-AZ VPC (AWS)

This project provisions a highly available Multi-AZ VPC architecture in AWS using Terraform.

---

## 🏗️ Architecture Overview

* VPC with CIDR block `10.0.0.0/16`
* 2 Availability Zones
* Public and Private subnets in each AZ
* Internet Gateway for public access
* NAT Gateway per AZ for private subnet outbound access
* Route tables for traffic routing

---

## 🌐 Architecture Flow

```
Internet
   ↓
Internet Gateway
   ↓
Public Subnets (AZ1, AZ2)
   ↓
NAT Gateways (one per AZ)
   ↓
Private Subnets (AZ1, AZ2)
```

---

## 🛠️ Technologies Used

* Terraform
* AWS (VPC, Subnets, NAT Gateway, Internet Gateway)

---

## 📁 Project Structure

```
terraform/
├── main.tf
├── variables.tf
├── provider.tf
├── outputs.tf
└── terraform.tfvars
```

---

## ⚙️ Prerequisites

* AWS Account
* Terraform installed
* AWS CLI configured

---

## ▶️ How to Run

```
terraform init
terraform plan
terraform apply
```

---

## 🧹 Cleanup

To avoid charges:

```
terraform destroy
```

---

## 💡 Key Features

* Multi-AZ high availability architecture
* Secure separation of public and private subnets
* NAT Gateway per AZ (no single point of failure)
* Scalable and reusable Terraform code

---

## ⚠️ Important Note

NAT Gateways incur cost. Always destroy resources after testing.

---

## 👨‍💻 Author

GitHub: https://github.com/sanjeeva26
