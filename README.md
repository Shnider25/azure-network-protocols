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
- Ubuntu Server 22.04

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
Initially, I installed an application called Wireshark. Wireshark functions as a protocol analyzer, providing the capability to inspect the generated traffic and its flow.
<br />

<p>
<img src="https://i.imgur.com/FF9wwAm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this context, I employed PowerShell to initiate a ping towards the private IP address of my secondary virtual machine. This action was intended to establish connectivity and generate ICMP traffic, enabling observation and analysis within Wireshark.
</p>
<br />
  <p>
<img src="https://i.imgur.com/YwBujZX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Subsequently, within the Azure interface, I navigated to the Network Security Group (NSG) settings of my second virtual machine. Here, I implemented a rule specifically designed to prohibit communication originating from other machines, thereby restricting incoming interactions.
  <p>
<img src="https://i.imgur.com/eDmYzZL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The continuous ping has ceased due to the implementation of the rule I established. Consequently, the communication pattern has shifted from the usual request-and-reply format to solely outgoing requests without receiving any corresponding replies.
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
