<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />






<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Step 1,  I began by creating a new Resource Group to organize the resources. Once the Resource Group is created, deploy a Windows 10 VM within it, configuring the necessary settings such as VM size, credentials, and enabling monitoring or backup. During the VM creation, allow Azure to automatically create a new Virtual Network (VNet) and Subnet for network isolation and communication. Afterward, deploy a Linux (Ubuntu) VM in the same Resource Group, configuring it with appropriate settings and SSH keys. Both VMs are placed in the same VNet to enable internal communication between them.




- Step 2
- Step 3
- Step 4

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src=https://i.imgur.com/KsvIYR3.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I configured a static IP on a Windows Server and installed Wireshark to capture and analyze ICMP network traffic between virtual machines in Azure. To validate the connection, I used the ping command in CMD and observed the ICMP traffic in Wireshark to confirm connectivity between the two machines.
</p>
<br />
