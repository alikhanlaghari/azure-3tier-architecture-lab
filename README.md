# Azure 3-Tier Architecture Lab (AZ-104)

## Overview
This project demonstrates a production-style 3-tier architecture in Microsoft Azure using secure network segmentation and controlled communication between tiers.

## Architecture
- Web Tier (Public)
- App Tier (Private)
- Database Tier (Highly Restricted)

## Components
- Azure Virtual Network (10.0.0.0/16)
- Subnets:
  - Web: 10.0.1.0/24
  - App: 10.0.2.0/24
  - DB:  10.0.3.0/24
- Network Security Groups (NSG)
- 3 Virtual Machines (Windows Server 2022)
- IIS Web Server

## Security Design
- Internet access only to Web Tier (port 80)
- Web → App allowed (port 80)
- App → DB allowed (port 1433)
- No direct public access to App and DB tiers

## Connectivity Flow
Internet → Web → App → Database

## Key Learnings
- Azure VNet and subnet design
- NSG-based traffic control
- Multi-tier architecture implementation
- Secure internal communication
- Jump host (bastion-style access)

## Screenshots
Refer to `/screenshots` folder for step-by-step implementation.
