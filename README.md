# Windows Server Home Lab with Active Directory and Domain Controller

## Description
This Home Lab details the process of creating a Windows Server virtual machine in VirtualBox, installing Active Directory, and promoting the server to Domain Controller.

## Project Walk-Through

### Part 1: VirtualBox Windows Server Active Directory Domain Controller and Static IP

To complete this lab, I installed VirtualBox to run my virtual machines. I started with the Windows Server virtual machine:

- **VM Name**: `EJC-DC-01`
- **OS**: Windows Server 2019
- **Memory Allocation**: 4 GB
- **Processor Allocation**: 2 processors

I downloaded the ISO file for Windows Server 2019 and installed Windows without a product key. After installation, I ran the following PowerShell command to generate a valid product key until 2038.

Next, I installed **Active Directory Domain Services** via Server Manager by navigating to:
Manage > Add Roles and Features > Active Directory Domain Services


After this, I promoted the server to Domain Controller by navigating to:
Flag > Promote this server to Domain Controller


I named the domain `ejc.local` and completed the **AD DS Configuration Wizard**.

#### Setting the Static IP Address

I set the virtual machine to a static IP address:

1. Clicked on **Ethernet Settings** under the Local Server tab in Server Manager.
2. Navigated to:
Network Connections > Ethernet > Properties > Internet Protocol Version 4 (TCP/IPv4) > Properties

3. Changed the IP address to `10.0.2.64` and the subnet mask to `255.255.255.0`.
4. Used the Command Prompt to find the default gateway (`10.0.2.2`) using `ipconfig` and changed the gateway accordingly.

#### Final Network Settings
Below are the final settings for the Ethernet connection after configuring the static IP address in the Control Panel:

- **IP Address**: 10.0.2.64
- **Subnet Mask**: 255.255.255.0
- **Default Gateway**: 10.0.2.2

### Part 2: Additional Information

#### Languages and Utilities Used
- **Active Directory**
- **PowerShell**
- **Command Line**

#### Environments Used
- **VirtualBox**
- **Microsoft Server 2019**

## Resources
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- [Microsoft Server 2019](https://www.microsoft.com/en-us/evalcenter/download-windows-server-2019)

## Works Cited
- [MassGrave](https://massgrave.dev/)
- [Reddit](https://www.reddit.com/r/sysadmin/comments/15pkzym/windows_server_2019_license/)
- [GitHub](https://github.com/JonCyberGuy/ActiveDirectoryLab/blob/main/README.md?plain=1)

## Image Information

### Ethernet Settings
![Ethernet Settings](image-link-1)

### Domain Controller Setup
![Domain Controller Setup](image-link-2)

---

HomeLab1  
Christian Gower
