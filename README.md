# Active-Directory-DS

A hands-on Windows Server and Active Directory lab built to develop practical systems administration skills, explore enterprise identity management, and gain experience configuring and managing a Windows domain environment.

## Project Overview

This project documents the deployment and administration of a virtualized Windows Server environment using Oracle VirtualBox.

The primary objective was to gain hands-on experience with Active Directory Domain Services (AD DS) and common administrative tasks performed in a Windows domain environment.

Throughout this lab, I configured Windows Server, deployed Active Directory, managed domain users and security groups, organized directory objects using Organizational Units (OUs), and implemented password policies. I also used PowerShell to perform server configuration and automate portions of the Active Directory setup.

This repository serves as a technical record of the lab environment, implementation process, configurations, and lessons learned.

## Objectives

- Deploy and configure a virtualized Windows Server environment.
- Configure static IP addressing and DNS.
- Install and configure Active Directory Domain Services.
- Establish a Windows domain environment.
- Join a Windows client machine to the domain.
- Manage domain users, security groups, and Organizational Units.
- Configure and apply Fine-Grained Password Policies.
- Develop PowerShell skills through server configuration and administrative tasks.
- Document implementation steps, configurations, and troubleshooting.

## Lab Environment

The lab was built using virtual machines to simulate a small Windows domain environment.

| Component | Configuration |
|---|---|
| Virtualization | Oracle VirtualBox |
| Server OS | Windows Server 2025 |
| Client OS | Windows 11 Enterprise |
| Directory Services | Active Directory DS |
| DNS | Windows Server DNS |
| Administration Tools | PowerShell and Active Directory Users and Computers (ADUC) |
| Scripting |  PowerShell |

## Technologies & Tools

- Oracle VirtualBox: Virtualization platform used to deploy and manage the lab environment.

- Windows Server 2022: Server operating system used to host domain services.

- Active Directory Domain Services (AD DS): Directory service used to manage domain resources, users, and authentication.

- DNS: Configured to support domain name resolution and Active Directory functionality.

- PowerShell: Used for server configuration, Active Directory deployment, and administrative tasks.

- Active Directory Users and Computers (ADUC): Graphical management console used to administer directory objects.

- Windows 11 Enterprise: Client operating system used to test domain connectivity and domain membership.

## Implementation

### 1. Virtual Machine Deployment & Network Configuration

Created and configured virtual machines in Oracle VirtualBox to establish the lab environment.

Tasks performed:

- Deployed Windows Server 2022 and Windows 11 Enterprise virtual machines.

- Configured the server with a static IP address.

- Configured DNS settings to support the domain environment.

- Established network connectivity between the virtual machines.

### 2. Windows Server Core Configuration

Configured Windows Server Core using PowerShell to gain experience administering Windows Server without relying on the full graphical interface.

Tasks performed:

- Configured initial server settings.

- Assigned static IP addressing.

- Configured DNS settings.

- Used PowerShell to perform server administration tasks.

### 3. Active Directory Domain Services Deployment

Installed and configured Active Directory Domain Services to establish the Windows domain environment.

Tasks performed:

- Installed AD DS.

- Configured Active Directory using a PowerShell script.

- Promoted the server to a domain controller.

- Configured the domain environment.

- Used Active Directory Users and Computers to manage directory objects.

4. Domain User & Organizational Unit Management

Practiced common Active Directory account and directory management operations.

Tasks performed:

- Created and managed domain user accounts.

- Created Organizational Units (OUs).

- Created security groups.

- Organized directory objects within OUs.

- Added users to security groups.

- Removed users from groups and deleted user accounts when appropriate.

- Practiced account lifecycle management.

5. Password Policy Management

Configured Fine-Grained Password Policies to explore more granular password policy administration in Active Directory.

Tasks performed:

- Created Password Settings Objects (PSOs).

- Configured password policy settings.

- Applied password policies to appropriate users or security groups.

- Practiced managing and verifying policy application.

6. Client Domain Integration

Configured a Windows client machine to participate in the domain environment.

Tasks performed:

Configured the Windows client to use the domain controller for DNS.

Joined the Windows 11 client to the Active Directory domain.

Practiced working with domain user accounts.

Verified domain connectivity and membership.

Skills Demonstrated

This project provided practical experience with:

Windows Server administration

Windows Server Core administration

Active Directory Domain Services

Domain controller configuration

DNS configuration

Static IP addressing

PowerShell administration and scripting

User and group lifecycle management

Organizational Unit administration

Security group management

Fine-Grained Password Policies

Windows domain integration

Virtual machine deployment and management

Technical documentation

Repository Structure

Active-Directory-Homelab/
│
├── README.md
│
├── Documentation/
│   ├── Environment-Setup.md
│   ├── Server-Configuration.md
│   ├── Active-Directory-Deployment.md
│   ├── User-and-Group-Management.md
│   └── Password-Policies.md
│
├── PowerShell/
│   ├── Configure-ServerCore.ps1
│   ├── Deploy-ActiveDirectory.ps1
│   ├── Create-Users.ps1
│   └── Create-Groups.ps1
│
└── Screenshots/
    ├── Server-Configuration/
    ├── Active-Directory/
    ├── User-and-Group-Management/
    └── Password-Policies/

The structure above is the intended organization. Files and folders will be added as the documentation and scripts are published.

Future Improvements

Potential expansions to this lab include:

Automating bulk user creation with PowerShell.

Implementing Group Policy Objects (GPOs).

Configuring shared folders and NTFS permissions.

Exploring Active Directory replication and additional domain controllers.

Implementing additional Windows Server infrastructure services.

Integrating Microsoft Entra ID and exploring hybrid identity.

Expanding into Microsoft Azure infrastructure.

Key Takeaways

This lab provided an opportunity to move beyond theoretical knowledge and practice administering a Windows domain environment.

Through configuring Windows Server, deploying Active Directory, managing directory objects, implementing password policies, and using PowerShell, I developed a stronger understanding of the infrastructure and identity management concepts used in enterprise IT environments.

This project is part of my ongoing effort to build practical systems administration, networking, automation, and cloud infrastructure skills.
