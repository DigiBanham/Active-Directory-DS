# Environment Setup

## Table of Contents

1. [Overview](#1-overview)
2. [Network Topology](#2-network-topology)
3. [System Requirements and Virtual Machine Configuration](#3-system-requirements-and-virtual-machine-configuration)
   - [3.1 Domain Controller — DC1](#31-domain-controller--dc1)
   - [3.2 Client Workstation — CLIENT1](#32-client-workstation--client1)
4. [Operating System Installation](#4-operating-system-installation)
   - [Operating System Verification](#operating-system-verification)
5. [Initial Network Verification](#5-initial-network-verification)
   - [5.1 Client Computer Identification](#51-client-computer-identification)
   - [5.2 Initial IP Configuration](#52-initial-ip-configuration)
6. [Outcome](#6-outcome)

## 1. Overview

This phase establishes the virtual infrastructure for the Active Directory homelab using Oracle VirtualBox. It covers the network topology, virtual machine requirements, resource allocation, and initial operating system installations.

The lab consists of two virtual machines:

- **DC1:** Windows Server 2025, designated to function as the domain controller and host the infrastructure services required for the lab.
- **CLIENT1:** Windows 11 Enterprise Evaluation, designated as the client workstation that will eventually join the Active Directory domain.

## 2. Network Topology

The lab environment follows the network topology illustrated below, including the network adapters, virtual network connections, and IP addresses planned for each machine.

![Active Directory Homelab Network Topology](../Screenshots/Environment-Setup/Network-Topology.png)

The domain controller will use two network adapters:

- **NAT:** Provides external network connectivity.
- **Internal Network:** Establishes an isolated network connection between the domain controller and client workstation.

The client workstation will connect to the same Internal Network as the domain controller.

DC1 will eventually provide Active Directory Domain Services (AD DS), DHCP, and routing services to support the lab environment.

## 3. System Requirements and Virtual Machine Configuration

Before deploying the virtual machines, I reviewed the lab's scope and objectives to identify the necessary operating system and hardware requirements.

Windows 11 Enterprise Evaluation was selected for the client workstation to support the planned Active Directory domain integration.

I also reviewed the system requirements for Windows Server 2025 and Windows 11, available on [learn.microsoft.com](https://learn.microsoft.com/en-us/), and allocated virtual hardware resources accordingly when creating the virtual machines in Oracle VirtualBox.

### 3.1 Domain Controller — DC1

| Configuration | Allocation |
|---|---|
| Operating System | Windows Server 2025 |
| VirtualBox VM Name | LabDC3 |
| Computer Name | DC1 |
| Memory (RAM) | 4096 MB |
| Processors | 4 |
| Network Adapter 1 | NAT |
| Network Adapter 2 | Internal Network |
| Virtual Disk | 50 GB |

![Windows Server 2025 Virtual Machine Configuration](../Screenshots/Environment-Setup/Server-VM-Configuration.png)

### 3.2 Client Workstation — CLIENT1

| Configuration | Allocation |
|---|---|
| Operating System | Windows 11 Enterprise Evaluation |
| VirtualBox VM Name | LabClient3 |
| Computer Name | CLIENT1 |
| Memory (RAM) | 4096 MB |
| Processors | 4 |
| Network Adapter 1 | Internal Network |
| Virtual Disk | 80 GB |

![Windows 11 Client Virtual Machine Configuration](../Screenshots/Environment-Setup/Client-VM-Configuration.png)

## 4. Operating System Installation

After creating the virtual machines and allocating their resources, I proceeded with clean installations of both operating systems.

- Installed Windows Server 2025 on the DC1 virtual machine.
- Installed Windows 11 Enterprise Evaluation on the CLIENT1 virtual machine.

Following installation, I verified the operating system versions to confirm that both machines were running the intended editions.

### Operating System Verification

**DC1 — Windows Server 2025**

![Windows Server 2025 System Information](../Screenshots/Environment-Setup/Server-OS-Verification.png)

**CLIENT1 — Windows 11 Enterprise Evaluation**

![Windows 11 System Information](../Screenshots/Environment-Setup/Client-OS-Verification.png)

## 5. Initial Network Verification

### 5.1 Client Computer Identification

Following the Windows 11 installation, I renamed the client computer to **CLIENT1** to establish a consistent naming convention throughout the lab.

Steps performed:

1. Right-click the Start button.
2. Select **System**.
3. Select **Rename this PC**.
4. Enter `CLIENT1` and complete the renaming process.

### 5.2 Initial IP Configuration

I used the `ipconfig /all` command on the client workstation to inspect its initial network configuration.

The results returned an Automatic Private IP Addressing (APIPA) address in the `169.254.x.x` range.

![CLIENT1 Initial IP Configuration](../Screenshots/Environment-Setup/Client-Initial-IP-Configuration.png)

This behavior was expected because the Internal Network did not yet have a DHCP server configured to assign IPv4 addresses to client devices.

At this stage, the virtual network infrastructure was established, but IP address assignment and client-server connectivity had not yet been configured or verified.

The next phase covers the initial Windows Server configuration, including static IP addressing and the deployment of the necessary network services to establish communication between the server and client virtual machines.

## 6. Outcome

The initial virtual infrastructure was successfully deployed, establishing the foundation for the subsequent configuration of Windows Server and Active Directory services.

The following tasks were completed:

- Designed the lab network topology.
- Created the DC1 and CLIENT1 virtual machines in Oracle VirtualBox.
- Allocated virtual hardware resources.
- Configured the domain controller with NAT and Internal Network adapters.
- Connected the client workstation to the same Internal Network.
- Completed clean installations of Windows Server 2025 and Windows 11 Enterprise Evaluation.
- Renamed the client workstation to CLIENT1.
- Verified the installed operating system versions.
- Inspected the client's initial IP configuration and identified the expected APIPA address.

The environment is now ready for the next phases: configuring the Windows Server infrastructure and establishing the network services required for client connectivity.