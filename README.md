<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


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

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
(Configuring a Firewall [Network Security Group)
 Initiate a perpetual/non-stop ping from your Windows 10 VM to your Ubuntu VM

1. Open the Network Security Group your Ubuntu VM is using and disable incoming (inbound) ICMP traffic

2. Back in the Windows 10 VM, observe the ICMP traffic in WireShark and the command line Ping activity

3. Re-enable ICMP traffic for the Network Security Group your Ubuntu VM

4. Back in the Windows 10 VM, observe the ICMP traffic in WireShark and the command line Ping activity (should start working)

5. Stop the ping activity</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Observe DHCP Traffic

1. In Wireshark, filter for DHCP traffic only

2. From your Windows 10 VM, attempt to issue your VM a new IP address from the command line

3. Open PowerShell as admin and run: ipconfig /renew

4. Observe the DHCP traffic appearing in WireShark</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Observe DNS Traffic

1. In WireShark filter for DNS traffic only

2. From your Windows 10 VM within a command line, use nslookup to see what google.com and disney.com's IP addresses are

3. Observe the DNS traffic being show in
WireShark</p>
<br />
