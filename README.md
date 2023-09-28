<p align="center">
</p>

<h1>Rooting an Unlocked Pixel 4a</h1>
In this tutorial, we obtain root access to a Pixel 4a. <br />



<h2>Environments and Technologies Used</h2>

- Carrier unlocked Pixel 4a running Sunfish v13.0
- Various command line tools
- Windows-android USB drivers
- Android Platform Tools
- Android Fastboot drivers

<h2>Operating Systems Used </h2>

- Windows 10 
- Sunfish 13.0

<h2>High-Level Steps</h2>

- Step 1: Unlock Bootloader on Pixel 4a
- Step 2: Install Magisk
- Step 3: Obtain and patch Sunfish 13.0 
- Step 4: Flash patched OS onto Pixel 4a

<h2>Actions and Observations</h2>

<p>
<img src="https://github.com/MerrickAM/azure-network-protocols/assets/145412020/70b17bd4-4c9a-4513-9c26-4ec46c18ff25"/>
</p>
<p>
  We start by creating our resources in Azure, making sure to allow ample time for virtual networks to be created. A common issue in setting these up through azure is not allowing enough time for resources to be created and we need to ensure that both virtual machines are on the same network.
</p>
<br />

<p>
<img src="https://github.com/MerrickAM/azure-network-protocols/assets/145412020/398ed29a-7d8c-45ba-9cc3-d18f2a508bbd"/>
</p>
<p>
Next, we will remote in to the windows machine to install wireshark. This is a generic install.
</p>
<br />

<p>
<img src="https://github.com/MerrickAM/azure-network-protocols/assets/145412020/3b89109e-0713-4090-a876-8044760c9cba"/>
</p>
<p>
Now we will attempt to ping the Linux machine using it's private IP address and observe the ICMP traffic in wireshark.
</p>
<br />

<p>
<img src="https://github.com/MerrickAM/azure-network-protocols/assets/145412020/266ba1a5-ec71-469d-b7db-c8fd6f62c132"/>
</p>
<p>
Create a new firewall rule through Azure to deny all ICMP traffic for the Linux machine and observe the change in Wireshark.
</p>
<br />

<p>
<img src="https://github.com/MerrickAM/azure-network-protocols/assets/145412020/c1cf955c-9394-4646-9d4f-bef23487bea2"/>
</p>
<p>
Here, We've used SSH through the command line to connect to the linux machine and observe the traffic within wireshark.
</p>
<br />

<p>
<img src="https://github.com/MerrickAM/azure-network-protocols/assets/145412020/6673e062-9332-4cfd-b6ca-ec42f56e4f6f)"/>
</p>
<p>
Now, we'll observe DHCP protocal by using the command "ipconfig /renew" in the windows machine to attempt to reassign it an IP address.
</p>
<br />

<p>
<img src="https://github.com/MerrickAM/azure-network-protocols/assets/145412020/9ffa8726-ebda-423e-9695-5fa78d4edef9)"/>
</p>
<p>
Finally, we'll use "nslookup google.com" to observe DNS traffic as the server gives us the IP for google.com.
</p>
<br />
