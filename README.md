# AWS Transit Gateway: Provider-Customer VPC Connectivity

## Project Overview

This project demonstrates the implementation of **AWS Transit Gateway** to securely connect two VPCs: a **Provider VPC** (`10.0.0.0/16`) and a **Customer VPC** (`192.168.0.0/16`) using the **AWS Console**. The setup enables communication between EC2 instances located in private subnets across both VPCs.

## Architecture Highlights

- **Transit Gateway** was used as the central hub for VPC-to-VPC communication.
- **Provider VPC**
  - CIDR: `10.0.0.0/16`
  - Private subnet: `10.0.2.0/24` with private EC2 instance
- **Customer VPC**
  - CIDR: `192.168.0.0/16`
  - Public subnet: `192.168.1.0/24` with public EC2 (used for SSH)
  - Private subnet: `192.168.2.0/24` with private EC2 instance
- SSH connection was made from the **public EC2** in Customer VPC to the **private EC2**.
- Successful **ICMP ping** from the private EC2 in Customer VPC to the private EC2 in Provider VPC validated connectivity.

## Key Components

- **AWS Transit Gateway**
- **Two VPCs** in the same AWS account
- **Route Tables** updated to route traffic via Transit Gateway
- **Security Groups** and **NACLs** configured to allow ICMP/SSH traffic
- **Bastion Host** used to securely access private instances

## Skills Demonstrated

- AWS Transit Gateway configuration
- VPC and subnet design
- Secure access using public bastion host
- EC2 provisioning and connectivity testing
- Route table and security configurations

## Author

Mohaned Mohamed  
Glasgow, United Kingdom  
m.gorashi282@gmail.com | +447417414418  
[LinkedIn Profile](https://www.linkedin.com/) | [GitHub Profile](https://github.com/)