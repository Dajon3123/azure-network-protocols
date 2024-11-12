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




- Step 2, I began by using Remote Desktop to connect to the Windows 10 Virtual Machine (VM). Once connected, install Wireshark on the Windows VM and open it to start packet capture. In Wireshark, set a filter to capture only ICMP traffic. Next, retrieve the private IP address of the Ubuntu VM and attempt to ping it from the Windows 10 VM, observing the ping requests and replies in Wireshark. Finally, open the command line or PowerShell on the Windows 10 VM, ping a public website (like www.google.com), and monitor the outbound traffic in Wireshark.
- Step 3, I began by logging in and Initiating a continuous ping from your Windows 10 VM to the Ubuntu VM. Then, open the Network Security Group (NSG) associated with the Ubuntu VM and disable inbound ICMP traffic. Return to the Windows 10 VM and observe the impact in both Wireshark (no ICMP traffic) and the command line (ping fails). Next, re-enable ICMP traffic for the Ubuntu VM's NSG, and observe the recovery of ping activity in Wireshark and the command line (pings should succeed). Finally, stop the continuous ping activity.
- Step 4, I ended this lab by doing some network traffic examination i began by logging into the Windows VM and started a Wireshark packet capture, filtering for SSH traffic. I then SSHed into the Ubuntu VM using ssh labuser@<private IP address> in PowerShell and observed the traffic in Wireshark. After exiting the SSH session by typing ‘exit,’ I filtered for DHCP traffic and ran ipconfig /renew in PowerShell to request a new IP address, watching the DHCP traffic appear in Wireshark. Next, I filtered for DNS traffic and used nslookup to query the IP addresses of google.com and disney.com, observing the DNS traffic. Finally, I filtered for RDP traffic (tcp.port == 3389) and noted the constant stream of data, as RDP maintains a live connection between the systems.

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
