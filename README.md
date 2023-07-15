# VMs-Traffic-Observing
This list will show and explain how to filter for the various internet traffic that occurs between the two Virtual Machines



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Wireshark
- Command Prompt

<h2>Operating Systems Used </h2>

- Windows 10 Pro</b> (22H2)
- [Linux] Ubuntu Server</b> (20.04 LTS)

<h2>List of Prerequisites</h2>

- Microsoft Azure
- Windows 10 Pro</b> (22H2) Virtual Machine
- [Linux] Ubuntu Server</b> (20.04 LTS) Virtual Machine
- Wireshark (Downloaded and Installed)

<h2>Internet Traffic Observation Objectives</h2>

- Observe ICMP Traffic
- Observe SSH Traffic
- Observe DHCP Traffic
- Observe DNS Traffic
- Observe RDP Traffic
  <p></p>

<h3>Observing ICMP Traffic</h3>

- Using Wireshark, filter specifically for ICMP Traffic only
  
<img src="https://i.imgur.com/4jZaKU1.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

 - Retrieve the private IP address of your Linux VM (from Microsoft Azure) and attempt to ping it from your Windows VM, using command line.

<img src="https://i.imgur.com/K8YLqks.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>  

<img src="https://i.imgur.com/ahnK1Bi.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

 - Observe the ping traffic within Wireshark.

<img src="https://i.imgur.com/FQaVZZn.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

 - In the Windows 10 VM, attempt to ping a public website and also observe the traffic in Wireshark. In this scenario, we'll ping www.goog.ecom.com
 - 
<img src="https://i.imgur.com/b1zaZGG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

</p>
<p>

 - Begin a perpetual ping to the Linux VM from the Windows 10 VM and take notice of the traffic in Wireshark.

<img src="https://i.imgur.com/WQtqqF4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/ljyRD2r.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

 - In MIcrosoft Azure, disable the inboud ICMP traffic on the Linux VM and monitor the traffic stopping in the Windows 10 VM.

<img src="https://i.imgur.com/6tCEVzv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/tQqvTRa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/bYWv2Wo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

 - After monitoring the traffic come to a halt, re-enable the ICMP traffic for the Linux and monitor it come back on.

<img src="https://i.imgur.com/Fiv7IEM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/8ZoDM52.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/0duEsS9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

 - Stop the ping activity, using Ctrl+C on the command prompt



</p>
<br />

<h4>Observing SSH Traffic</h4>

 - In WireShark, clear ICMP and filter for SSH traffic only

<img src="https://i.imgur.com/2EVU5hb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

 - Within the Windows 10 VM Command Line, "SSH into" your Linux Virtual Machine, using the Linux Private IP address and Administrator password.

<img src="https://i.imgur.com/ELoxIFz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

 - Run a few commands (username, pwd, etc) in the Linux SSH connection and monitor the SSH traffic spam in WireShark.

<img src="https://i.imgur.com/qDyI3NJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

 - Exit the SSH connection by typing 'exit' and pressing [Enter}

<img src="https://i.imgur.com/Hhfnf5B.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<h4>Observing DHCP Traffic</h4>

 - In WireShark, clear ICMP and filter for DHCP traffic only.

<img src="https://i.imgur.com/Hla1CK5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

 - From the Windows 10 VM, attempt to issue the VM a new IP within Command Line (ipconfig /renew) and notice the DHCP traffic appearing in WireShark

<img src="https://i.imgur.com/1ONtdC0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>



<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

</p>
<br />

<h4>Observing DNS Traffic</h4>

 - In WireShark, clear DHCP and filter for DNS Traffic only

<img src="https://i.imgur.com/h1SMP3N.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

 - From within the Windows 10 VM Command Line, find google.com and disney.com's IP addresses, using nslookup

<img src="https://i.imgur.com/6dSd68x.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

 - Observe the DNS traffic being shown in WireShark

<img src="https://i.imgur.com/TUIjAsV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>
<p>

<h4>Observing RDP Traffic</h4>

 - In WireShark, clear DHCP and filter for RDP traffic only (tcp.port ==3389)



 - Observe the constant spam of traffic that is transmitted from one computer to another


<h4>Close the Remote Desktop Connection and delet the Resource groups</h4>


</p>
<br />
