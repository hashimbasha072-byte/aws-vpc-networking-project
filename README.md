# AWS VPC Networking Project

## 📌 Project Overview

This project demonstrates hands-on experience with **Amazon VPC networking** by creating a custom VPC environment and configuring the required networking components to allow communication between AWS resources.

The project covers VPC creation, subnet configuration, route tables, Internet Gateway, EC2 deployment, security groups, and VPC peering.

---

## 🏗️ Architecture

```text
                         Internet
                            |
                            v
                    Internet Gateway
                            |
                            v
                    Custom VPC
                            |
              +-------------+-------------+
              |                           |
              v                           v
        Public Subnet               Private Subnet
              |                           |
              v                           v
         EC2 Instance                AWS Resource
```

A separate VPC was also configured for **VPC Peering** to demonstrate private communication between VPC networks.

---

## ☁️ AWS Services Used

* Amazon VPC
* Subnets
* Route Tables
* Internet Gateway
* Amazon EC2
* Security Groups
* VPC Peering
* Amazon Linux

---

## ⚙️ Implementation

### 1. Create a Custom VPC

Created a custom VPC with a dedicated CIDR block.

Example:

```text
VPC CIDR: 10.0.0.0/16
```

The VPC provides an isolated virtual network for AWS resources.

---

### 2. Create Subnets

Created subnets inside the VPC for organizing AWS resources.

Example:

```text
VPC
│
├── Public Subnet
│
└── Private Subnet
```

The subnets were configured with appropriate CIDR ranges.

---

### 3. Create Internet Gateway

Created and attached an **Internet Gateway (IGW)** to the VPC.

The Internet Gateway provides a path between the VPC and the internet for resources configured for internet connectivity.

---

### 4. Configure Route Table

Created and configured a route table for the public subnet.

Example route:

```text
Destination: 0.0.0.0/0
Target: Internet Gateway
```

Associated the route table with the appropriate subnet.

---

### 5. Launch EC2 Instance

Launched an Amazon EC2 instance inside the configured VPC/subnet.

The instance was used to verify the networking configuration and connectivity.

---

### 6. Configure Security Group

Configured an EC2 security group to control inbound and outbound traffic.

Example inbound rules:

```text
SSH  - TCP - 22
HTTP - TCP - 80
```

Only the required ports were opened for testing and application access.

---

### 7. Test Connectivity

Verified connectivity between the EC2 instance and the configured network components.

The configuration was tested to ensure that the routing and security rules worked as expected.

---

## 🔗 VPC Peering

Configured **VPC Peering** between two VPC networks to demonstrate private communication.

Example:

```text
VPC A
CIDR: 10.0.0.0/16
       |
       | VPC Peering
       |
       v
VPC B
CIDR: 10.1.0.0/16
```

The required routes were configured in the route tables of both VPCs.

This allows resources in the peered VPCs to communicate using private IP addresses, subject to the configured routing and security rules.

---

## 🔄 Network Flow

```text
Internet
   |
   v
Internet Gateway
   |
   v
Route Table
   |
   v
Public Subnet
   |
   v
EC2 Instance
   |
   v
Security Group
```

For VPC peering:

```text
VPC A
  |
  | Private Network Communication
  |
VPC Peering Connection
  |
  |
VPC B
```

---

## 🧪 Hands-On Tasks Completed

* Created a custom VPC
* Configured CIDR blocks
* Created subnets
* Created route tables
* Attached an Internet Gateway
* Associated subnets with route tables
* Launched EC2 instances inside the VPC
* Configured security groups
* Tested network connectivity
* Configured VPC peering
* Updated routing for VPC-to-VPC communication

---

## 📚 Key Concepts Learned

This project provided practical understanding of:

* AWS VPC architecture
* CIDR notation
* Public and private subnets
* Route tables
* Internet Gateway
* Security Groups
* EC2 networking
* VPC Peering
* Private IP communication
* AWS network routing
* Basic cloud network security

---

## 🎯 Project Outcome

Successfully created and configured an AWS VPC networking environment with subnets, route tables, an Internet Gateway, EC2 instances, security groups, and VPC peering.

This project strengthened practical understanding of **AWS networking, EC2 connectivity, routing, and foundational cloud infrastructure concepts**.

---

## 🛠️ Technologies

```text
AWS
Amazon VPC
Amazon EC2
Subnets
Route Tables
Internet Gateway
Security Groups
VPC Peering
Amazon Linux
```

---

## 👨‍💻 Author

**A Mohammed Hashim**

BCA Graduate | AWS | Cloud Computing | DevOps | SRE

GitHub: https://github.com/hashimbasha072-byte
