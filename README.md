<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Powershell. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04


<h2>Actions and Observations</h2>

![Screenshot 2025-03-03 201614](https://github.com/user-attachments/assets/a85b12b3-ff03-41f1-9922-61657bccefb1)


<p>
 Initiate a ping from your Windows 10 VM to your Ubuntu VM

1. Open the Network Security Group your Ubuntu VM is using and disable incoming (inbound) ICMP traffic

2. Back in the Windows 10 VM, observe the ICMP traffic in WireShark and the command line Ping activity

3. Re-enable ICMP traffic for the Network Security Group your Ubuntu VM

4. Back in the Windows 10 VM, observe the ICMP traffic in WireShark and the command line Ping activity (Powershell)

5. Stop the ping activity</p>
<br />


![Screenshot 2025-03-03 202358](https://github.com/user-attachments/assets/a8b4893d-a750-4161-8ad8-a047ffdb9d3d)



Observe DHCP Traffic

1. In Wireshark, filter for DHCP traffic only

2. From your Windows 10 VM, attempt to issue your VM a new IP address from the command line

3. Open PowerShell as admin and run: ipconfig /renew

4. Observe the DHCP traffic appearing in WireShark</p>
<br />


![Screenshot 2025-03-03 202732](https://github.com/user-attachments/assets/23b38c0b-66a7-4683-b1b1-53862635729b)



Observe DNS Traffic

1. In WireShark filter for DNS traffic only

2. From your Windows 10 VM within a command line, use nslookup to see what google.com and disney.com's IP addresses are

3. Observe the DNS traffic being show in
WireShark</p>
<br />
