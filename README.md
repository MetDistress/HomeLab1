# HomeLab1 - Windows Server Home Lab with Active Directory and Domain Controller
## Purpose
The purpose of this home lab is to advance my knowledge of Windows Server, Active Directory, and Systems Administration.
## Project Summary
To complete this lab, I have installed VirtualBox to run my virtual machines. I started with the Windows Server virtual machine. I spun up a new virtual machine in VirtualBox named EJC-DC-01 and selected Windows 2019 as the operating system. I downloaded the ISO file for Windows Server 2019 and allocated 4 GB of memory and 2 processors. Following this, I booted up the VM, and installed Windows without a product key. After this, I ran the following command in PowerShell and generated a product key that was valid until the year 2038. <br>
<p align="center">
<img src="HomeLab1_Pics\powershell_windows_product_key.png" alt="irm https://massgrave.dev/get | iex"> </p><br>
I now had a Windows Server Virtual Machine with a valid product key. Following this, through server manager, I navigated to Manage > Add Roles and Features, and installed Active Directory Domain Services. After this I navigated to the Flag > Promte this server to Domain Controller. I named the domain ejc.local and finished going through the AD DS Configuration Wizard. 
## Languages and Utilities Used
## Environments Used
## Resources
VirtualBox: <br>
Microsoft Server 2019: <br>
## Works Sited
  MassGrave: https://massgrave.dev/<br>
  Reddit: https://www.reddit.com/r/sysadmin/comments/15pkzym/windows_server_2019_license/<br>
  GitHub: https://github.com/JonCyberGuy/ActiveDirectoryLab/blob/main/README.md?plain=1
