# Azure Identity and RBAC Implementation Lab

## Overview
This project demonstrates how to implement identity management and role-based access control (RBAC) in Microsoft Azure using Microsoft Entra ID.

The lab simulates a small organization that must control access to its cloud infrastructure by assigning permissions based on job roles. Security groups are used to manage users, and RBAC roles are assigned at the resource group scope to enforce the principle of least privilege.

## Objective

The goal of this lab is to demonstrate how an Azure administrator can securely manage identities and permissions within an Azure environment.

This lab includes the following tasks:

* Deploy Azure infrastructure
* Create users in Microsoft Entra ID
* Organize users into security groups
* Assign RBAC roles based on job function
* Test access permissions across multiple identities

## Scenario

You are the Azure administrator for a small organization.

Your responsibility is to configure identity management and implement access controls that allow different teams to interact with Azure resources according to their roles.

The organization has three teams:

Team	Responsibility
IT Administrators	Manage infrastructure and virtual machines
Developers	View resources needed for application development
Auditors	Review infrastructure for compliance

Each team must be granted only the permissions necessary for their role.

## RBAC Role Mapping

The following RBAC roles were assigned to each group:

Security Group	Assigned Role	Scope
IT-Admins-Virtual Machine Contributor	
Developers- Reader
Auditors-Reader Subscription

These assignments enforce least privilege access while still allowing each team to perform their required tasks.

## Implementation Steps
1. Create Resource Group

A resource group was created to contain all infrastructure used in the lab.

Example configuration:

Resource Group Name: RG-Identity-Lab
Region: East US

2. Deploy Virtual Network

A virtual network was deployed to simulate an internal company network.

Configuration:

Virtual Network Name: VNET-Identity-Lab
Address Space: 10.10.0.0/16
Subnet: Subnet-Servers (10.10.1.0/24)

3. Deploy Virtual Machine

A Windows Server virtual machine was created to represent infrastructure managed by administrators.

Configuration:

VM Name: VM-Admin-Test
Operating System: Windows Server 2022
Public IP: Enabled

4. Create Users in Microsoft Entra ID

Three test users were created to represent different roles within the organization.

Users created:

adminuser
devuser
audituser
5. Create Security Groups

Security groups were created to organize users by job function.

Groups created:

IT-Admins
Developers
Auditors
6. Assign Users to Groups

Users were assigned to groups according to their responsibilities.

7. Configure RBAC Permissions

RBAC roles were assigned to the security groups at the resource group scope.

Assignments:

IT-Admins → Virtual Machine Contributor
Developers → Reader
Auditors → Reader

This ensures that permissions are managed at the group level instead of per user.

## Testing Access Control

To verify the RBAC configuration, access was tested using different user accounts.

Developer Test

User: devuser

Attempted action:

Start virtual machine

Result:

Access denied

Developers only have read permissions.

## Administrator Test

User: adminuser

Attempted actions:

Start virtual machine
Stop virtual machine
Restart virtual machine

Result:

Access granted

## Key Security Concepts Demonstrated

This lab demonstrates several important cloud security principles:

Identity and access management
Role-based access control (RBAC)
Security group administration
Least privilege access
Permission scope management
Learning Outcomes

## After completing this lab, the following skills were demonstrated:

Managing identities using Microsoft Entra ID
Implementing RBAC roles in Azure
Structuring access using security groups
Deploying and managing Azure infrastructure
Validating role permissions through access testing
