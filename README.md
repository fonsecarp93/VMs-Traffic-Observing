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

 - In the Windows 10 VM, attempt to ping a public website and also observe the traffic in Wireshark. In this scenario, we'll ping www.disney.com
 - 
<img src="https://i.imgur.com/Xp17yWD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/Xp17yWD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<h4>Observing SSH Traffic</h4>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<h4>Observing DHCP Traffic</h4>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<h4>Observing DNS Traffic</h4>


<h4>Observing RDP Traffic</h4>


Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
