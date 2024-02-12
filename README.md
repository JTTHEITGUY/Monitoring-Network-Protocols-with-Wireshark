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
- Linux Ubuntu

<h2>List of Prerequisites</h2>

- Microsoft Azure Subscription
- Wireshark
- Microsoft Windows PC 
- Windows Powershell 
- Microsoft Azure -(Resource Group, 2 Virtual Machines, and a Virtual Network.)


<h2>Installation Steps</h2>

<p>

</p>
<p>

  **Step 1: Create a Resource Group**
Create a Resource Group using the Azure Portal website (A resource group can also be created using the Azure CLI, see my other tutorial for that method)

<p>
 
![Optional Image Description](https://i.imgur.com/LOwHRpB.png)

</p>
<p>

**Step 2: Create a Windows 10 Virtual Machine (VM)**

a. While creating the VM, select the previously created Resource Group
![Optional Image Description](https://i.imgur.com/EwZsxsu.png)

![Optional Image Description](https://i.imgur.com/QX826qw.png)

**Step 3: Create a Linux (Ubuntu) VM**

![Optional Image Description](https://i.imgur.com/QJHHoF4.png)


a. While creating the VM, select the previously created Resource Group and VNET
![Optional Image Description](https://i.imgur.com/5Mb6ZpM.png)

</p>
<br />

<p>


</p>
<p>

**Step 4: Observe Your Virtual Network Topology within Network Watcher**

![Optional Image Description](https://i.imgur.com/LzEPu0l.png)

</p>
<br />

<p>

</p>
<p>

**Step 5: Observe ICMP Traffic**

a. Use Remote Desktop to connect to your Windows 10 Virtual Machine
![Optional Image Description](https://i.imgur.com/7ZaXV8t.png)

b. Within your Windows 10 Virtual Machine, Install Wireshark
![Optional Image Description](https://i.imgur.com/P9hH2WW.png)
</p>
<br />

<p>



</p>
<p>


