<p align="center">


</p>
<p>


![Optional Image Description](https://i.imgur.com/QtpsAu1.png)

</p>
<p>

<h1>Monitoring Network Protocols with Wireshark</h1>
This tutorial details the prerequisites and installation steps for Wireshark and explains how to use it to monitor various network protocols and view real-time network traffic using two virtual machines in Microsoft Azure.


<h2>Environments and Technologies Used</h2>

- Microsoft Azure 
- Wireshark
- Windows Powershell

<h2>Operating Systems Used </h2>

- Windows 10</b> 
- Ubuntu Linux 

<h2>List of Prerequisites</h2>

- Microsoft Azure Subscription
- Wireshark
- Microsoft Windows PC 
- Windows Powershell 
- Microsoft Azure (1 Resource Group, 2 Virtual Machines, and a Virtual Network)


<h2>Installation Steps</h2>

<p>

</p>
<p>

  **Step 1: Create a Resource Group**

Create a Resource Group using the Azure Portal website (A resource group can also be created using the Azure CLI, see my other tutorial for that method)

<p>
 
![Optional Image Description](https://i.imgur.com/plCEaAE.png)

</p>
<p>

**Step 2: Create a Windows 10 Virtual Machine (VM)**

a. While creating the Virtual Machine, select the previously created Resource Group.
![Optional Image Description](https://i.imgur.com/8h0Ub2J.png)

![Optional Image Description](https://i.imgur.com/sXMyTiM.png)

**Step 3: Create a Linux (Ubuntu) Virtual Machine**

![Optional Image Description](https://i.imgur.com/tt7aETc.png)


a. While creating the Virtual Machine, select the previously created Resource Group and VNET.
![Optional Image Description](https://i.imgur.com/zBnj4bX.png)

</p>
<br />

<p>


</p>
<p>

**Step 4: Observe Your Virtual Network Topology within Network Watcher**

![Optional Image Description](https://i.imgur.com/6Q346nw.png)

</p>
<br />

<p>

</p>
<p>

**Step 5: Connect to the Windows 10 Virtual Machine and install Wireshark**

a. Use Remote Desktop to connect to your Windows 10 Virtual Machine.
![Optional Image Description](https://i.imgur.com/yhAsPgP.png)

b. Within your Windows 10 Virtual Machine, Install Wireshark.
![Optional Image Description](https://i.imgur.com/P9hH2WW.png)
</p>
<br />

<p>



</p>
<p>

**Step 6: Open Wireshark and filter for ICMP traffic**

a. Retrieve the private IP address of the Ubuntu Virtual Machine and attempt to ping it from within the Windows 10 Virtual Machine.
![Optional Image Description](https://i.imgur.com/guFbACk.png)

b. Observe ping requests and replies within WireShark.
![Optional Image Description](https://i.imgur.com/YqhhMqu.png)
![Optional Image Description](https://i.imgur.com/GrI0fOx.png)
</p>
<br />

<p>


</p>
<p>


**Step 7: Initiate a perpetual/non-stop ping from your Windows 10 Virtual Machine to your Ubuntu Virtual Machine**

a. Open the Network Security Group your Ubuntu Virtual Machine is using and disable (deny) incoming (inbound) ICMP traffic.
![Optional Image Description](https://i.imgur.com/9mtkkZG.png)
![Optional Image Description](https://i.imgur.com/ntjVTQH.png)

b. Back in the Windows 10 Virtual Machine, observe the ICMP traffic in WireShark and the command line Ping activity (notice the perpetual ping has stopped due to inbound ICMP traffic being disabled).
![Optional Image Description](https://i.imgur.com/7XE35Ps.png)

c. Re-enable ICMP traffic for the Network Security Group your Ubuntu Virtual Machine is using.
![Optional Image Description](https://i.imgur.com/affJN79.png)

d. Back in the Windows 10 Virtual Machine, observe the ICMP traffic in WireShark and the command line Ping activity (it should resume working again).
![Optional Image Description](https://i.imgur.com/sQ68cVJ.png)

</p>
<br />

<p>


</p>
<p>

**Step 8: Observe SSH Traffic**

a. Back in Wireshark, filter for SSH traffic.
![Optional Image Description](https://i.imgur.com/Q3oE1RU.png)

b. From your Windows 10 Virtual Machine, “SSH into” your Ubuntu Virtual Machine (via its private IP address). Type commands (username, pwd, etc) into the Linux SSH connection and observe SSH traffic in WireShark.
![Optional Image Description](https://i.imgur.com/9l5TJrf.png)

</p>
<br />

<p>


</p>
<p>

**Step 9: Observe DHCP Traffic**

a. Back in Wireshark, filter for DHCP traffic.
![Optional Image Description](https://i.imgur.com/jyr6dnV.png)

b. From your Windows 10 Virtual Machine, attempt to issue your Virtual Machine a new IP address from the command line (ipconfig /renew) Observe the DHCP traffic appearing in WireShark.
![Optional Image Description](https://i.imgur.com/xjnyd9m.png)

</p>
<br />

<p>


</p>
<p>

**Step 10: Observe DNS Traffic**

a. Back in Wireshark, filter for DNS traffic.
![Optional Image Description](https://i.imgur.com/EvpYV5J.png)

b. From your Windows 10 within a command line, use nslookup to see the google.com IP address. Observe the DNS traffic being shown in WireShark.
![Optional Image Description](https://i.imgur.com/bQc22Gw.png)

</p>
<br />

<p>


</p>
<p>

Lab Cleanup (DON’T FORGET TO DO THIS)

a. Close your Remote Desktop connection.
![Optional Image Description](https://i.imgur.com/d0CPxJ6.png)

b. Delete the Resource Group(s) created at the beginning of this lab.
![Optional Image Description](https://i.imgur.com/ocMIuAZ.png)

A big shoutout to Course Careers and Josh Madakor for providing the inspiration for this lab!


