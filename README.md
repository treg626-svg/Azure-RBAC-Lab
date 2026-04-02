# Azure Identity and RBAC Lab

## Overview

This project demonstrates how to implement identity management and role-based access control in Microsoft Azure using Microsoft Entra ID.

The goal of this lab was to simulate how an organization controls access to infrastructure using security groups and RBAC.

## Project Objectives

- Create and manage users in Microsoft Entra ID
- Organize users into security groups
- Assign Azure RBAC roles based on job function
- Apply least-privilege access at the resource group scope
- Test access permissions across multiple identities

## Architecture

The RBAC model used in this lab demonstrates how Azure role-based access control organizes permissions through users and security groups inside a tenant.

![RBAC Architecture](architecture/architecture-diagram.png)

## Explanation

The environment follows a simple RBAC hierarchy:

This lab uses Microsoft Entra ID security groups to simplify access management.

- **IT-Admins** → **Virtual Machine Contributor**
- **Developers** → **Reader**
- **Auditors** → **Reader**

Role assignments were scoped at the **Resource Group** level to enforce the principle of least privilege.

• IT-Admins – infrastructure management    
• Developers – read-only access to resources  
• Auditors – visibility for compliance review  

Users were assigned to groups, and RBAC roles were applied at the Resource Group scope to enforce the principle of least privilege.

## Technologies Used

Microsoft Azure  
Microsoft Entra ID  
Azure Virtual Machines  
Azure RBAC  

## Skills Demonstrated

- Microsoft Entra ID administration
- Azure RBAC configuration
- Security group management
- Resource group scoping
- Least-privilege access design
- Azure VM deployment  

## Lab Components

Resource Group  
Virtual Network  
Virtual Machine  
Security Groups  
RBAC Roles  

## Learning Outcomes

Configured users and groups in Entra ID  
Assigned RBAC roles at the resource group scope  
Implemented least privilege access control  
Tested role permissions across multiple user accounts
