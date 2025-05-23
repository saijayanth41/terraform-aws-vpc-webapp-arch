# Terraform AWS VPC with Public/Private Subnets, NAT Gateway, and EC2 Instances

## 📦 Project Overview

This project provisions a complete **AWS Virtual Private Cloud (VPC)** architecture using Terraform. It is designed to simulate a real-world infrastructure setup with:

- A custom VPC
- Public and Private Subnets
- Internet Gateway and NAT Gateway
- Separate EC2 instances for WordPress (public) and MySQL (private)
- Custom Route Tables and Security Groups

---

## 🔧 Technologies Used

- **Terraform** for Infrastructure as Code (IaC)
- **AWS EC2** for compute resources
- **AWS VPC, Subnets, NAT Gateway, Route Tables**
- **AWS Security Groups** for traffic control

---

## 🗂️ Project Structure

```
.
├── main.tf               # Main infrastructure definition
├── variables.tf          # (Optional) Input variables for reusability
├── outputs.tf            # (Optional) Output definitions
├── README.md             # Project documentation
```

---

## 🚀 What It Does

- Creates a **custom VPC** (`192.168.0.0/16`)
- Sets up a **public subnet** (`192.168.0.0/24`) and **private subnet** (`192.168.1.0/24`)
- Associates an **Internet Gateway** for public internet access
- Deploys a **NAT Gateway** to allow outbound access from the private subnet
- Provisions:
  - A **WordPress EC2 instance** in the public subnet
  - A **MySQL EC2 instance** in the private subnet
- Configures:
  - Route tables for public and private subnets
  - Security Groups allowing HTTP/SSH access to the web server, and SQL access to the DB server

---

## ✅ Prerequisites

- AWS CLI configured with a profile named `jayanth`
- Terraform installed
- A valid AWS key pair (`saikey.pem`) available and referenced correctly

---

## 🛡️ Security Notes

- SSH (`22`) and HTTP (`80`) are open to all (`0.0.0.0/0`) for demonstration. Restrict access for production.
- MySQL port (`3306`) is secured by referencing the web server's security group.
- PEM files should be handled securely and **never pushed to GitHub**.

---

## 📌 How to Use

```bash
terraform init
terraform plan
terraform apply
```

---

## 🎯 Recruiter-Relevant Skills Demonstrated

- Infrastructure-as-Code with Terraform
- VPC networking and private/public subnet design
- NAT Gateway setup for secure internet access from private resources
- Security Group configuration and EC2 provisioning
- Real-world architecture with WordPress + MySQL separation

---

## 👤 Author

**Sai Jayanth Rajamahendram**  
Cloud | DevOps | Infrastructure as Code  
[LinkedIn](https://www.linkedin.com/in/saijayanthraj/) | [GitHub](https://github.com/saijayanth41)
