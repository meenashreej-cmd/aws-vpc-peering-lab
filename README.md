# AWS VPC Peering Lab

## 📌 Project Overview
This project demonstrates communication between two Virtual Private Clouds (VPCs) using AWS VPC Peering. It explores private network connectivity, route table configuration, security groups, and EC2 instance communication.

## 🎯 Objectives
- Create two VPCs with separate CIDR ranges.
- Configure public and private subnets.
- Establish VPC peering between the VPCs.
- Configure route tables and security groups.
- Test connectivity between private EC2 instances.
- Simulate a network failure and verify recovery.

## 🛠️ AWS Services Used
- Amazon VPC
- Amazon EC2
- VPC Peering
- Route Tables
- Security Groups
- Internet Gateway

## 🏗️ Architecture

**VPC A — 10.10.0.0/16**
- Public subnet: `10.10.1.0/24`
- Private subnet: `10.10.2.0/24`
- Bastion host: `10.10.1.10`
- Private EC2 instance: `10.10.2.10`

**VPC B — 10.20.0.0/16**
- Private subnet: `10.20.1.0/24`
- Private EC2 instance: `10.20.1.10`

The two VPCs communicate through an active VPC peering connection. Routes in both VPCs direct traffic for the remote CIDR range through the peering connection.

## 🧪 Testing and Results

| Test | Result |
|---|---|
| VPC peering connection | Active |
| App-A to App-B ping | Successful |
| App-B to App-A ping | Successful |
| Controlled ICMP failure | Verified |
| Connectivity after restoring the rule | Successful |
| Simulated route failure and recovery | Verified |

## 🔐 Security
- Private EC2 instances do not require public IP addresses.
- SSH access to private instances is routed through the bastion host.
- Security groups restrict traffic to specified sources.
- Private keys and credentials must not be committed to the repository.

## 📚 Key Learnings
- VPC and subnet configuration
- VPC peering and CIDR-based routing
- Forward and return routes
- Security group rules and ICMP troubleshooting
- Bastion-host access to private EC2 instances
- Network failure testing and recovery

## 📄 Project Report
The project report will be included in this repository after checking that it contains no sensitive information and that publication is permitted.

## 👩‍💻 Author
Meenashree Jagadeeshkumar
