<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we explore different network traffic involving Azure Virtual Machines by using Wireshark. Additionally, we experiment with Network Security Groups to enhance our understanding. <br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (22H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Step 1- Downloaded Wireshark
- Step 2- Use Powershell
- Step 3- Creating a NSG rule
- Step 4- Request timed out
- Step 5- SSH Protocol
- Step 6- SSH Traffic
- Step 7- DNS Protocol
<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/d0HTJ2Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I had recently installed an app name Wireshark, wireshark is a protocol analayzer which allows you to look at the traffic thats being generated and coming through as it goes.
</p>
<br />

<p>
<img src="https://i.imgur.com/G4Fi5k8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here I used Powershell to ping my second virtual machine's private IP address to get some connectivity to get some traffic going under ICMP to observe on Wireshark.
</p>
<br />
  
  <p>
<img src="https://i.imgur.com/mtkGa1j.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The non stop ping has now been timed out because of the rule that I created which is now not a request, reply but is not just a request with no replies.
</p>
<br />

<p>
<img src="https://i.imgur.com/NfsaXQQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this step, I am going to SSH( secure shell) into my second virtual machine via my first virtual machine using powershell!
</p>
<br />

<p>
<img src="https://i.imgur.com/3LfHa4s.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here I was creatign some traffic to inspect for SSH.
</p>
<br />

<p>
<img src="https://i.imgur.com/d4hehWO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here I am basically asking DNS(domain name system) what's google's IP address.
</p>
<br />
