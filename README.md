# AWS VPC Peering Project

## Project Overview
This project demonstrates secure network connectivity between two Amazon Virtual Private Clouds (VPCs) using AWS VPC Peering.

## Objectives
- Create two separate VPCs.
- Configure public and private subnets.
- Establish a VPC peering connection.
- Configure route tables for communication between VPCs.
- Configure security groups and a bastion host.
- Verify connectivity using SSH and ICMP ping tests.

## Architecture

| Component | VPC A | VPC B |
|---|---|---|
| VPC CIDR | `10.10.0.0/16` | `10.20.0.0/16` |
| Private subnet | `10.10.2.0/24` | `10.20.1.0/24` |
| Application instance | `10.10.2.10` | `10.20.1.10` |

A bastion host in VPC A provides SSH access to the private instances.

## Implementation
1. Created VPC A and VPC B with non-overlapping CIDR ranges.
2. Created the required subnets and route tables.
3. Established an active VPC peering connection.
4. Added routes for communication between the two VPCs.
5. Configured security groups to control access.
6. Connected to private instances through the bastion host.
7. Tested connectivity using ping commands.

## Verification
Successful ICMP ping tests were observed between the private application instances across the peering connection, with **0% packet loss** in the successful tests.

## Screenshots
See the screenshots uploaded to this repository for evidence of the VPC configuration, active peering connection, route tables, and connectivity tests.

## Technologies Used
- Amazon Web Services (AWS)
- Amazon VPC
- VPC Peering
- EC2
- Security Groups
- Route Tables
- SSH and ICMP

## Author
Piyush Das

