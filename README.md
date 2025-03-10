<p align="center">
<img src="https://github.com/user-attachments/assets/b0bd706b-d425-4897-bff6-5d1467b09cb8" height="80%" width="80%"/>
</p>

<h1>Practicing DNS</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- A-Record Exercise
- Local DNS Cache Exercise
- CNAME Record Exercise

<h2>Deployment and Configuration Steps</h2>

**A-Record exercise**
<p>
After logging into both the domain controller PC and the client PC as the administrator, ping "mainframe" and observe the failure.
</p> 
<p>
<img src="https://github.com/user-attachments/assets/e57bbf2f-1ec7-4127-902c-4820cad98ffe" height="80%" width="80%" /> 
</p>
<br />

<p>
Perform an nslookup for "mainframe" and notice that it fails (there is no DNS record).
</p> 
<p>
<img src="https://github.com/user-attachments/assets/e5a0850b-8002-4027-9a91-b3d3f4d6b723" height="80%" width="80%" /> 
</p>
<br />



<p>
 Create a DNS A-record on the domain controller for “mainframe” and have it point to the domain controller's Private IP address.
</p> 
<p>
<img src="https://github.com/user-attachments/assets/c1d02775-2e04-4528-904e-7c7cedb47928" height="80%" width="80%" /> <br /> <br />
<img src="https://github.com/user-attachments/assets/62d40226-6a8a-4db6-b9e5-aea29c327c8f" height="80%" width="80%" /> <br /> <br />
<img src="https://github.com/user-attachments/assets/cdb2e5bb-df1e-4e50-bb9e-dd4f2873b95d" height="80%" width="80%" /> <br /> <br /> 
<img src="https://github.com/user-attachments/assets/b8a01387-578f-449e-924f-05d1c5068b23" height="80%" width="80%" /> <br /> <br />
</p>
<br />



<p>
On the client PC, ping the "mainframe" and observe that it works.
</p> 
<p>
<img src="https://github.com/user-attachments/assets/2aa28bd9-3774-4518-9945-7f9277dd13ec" height="80%" width="80%" /> 
</p>
<br />



**Local DNS Cache Exercise**

<p>
On the client PC ping the "mainframe" and observe that it works.
</p> 
<p>
<img src="https://github.com/user-attachments/assets/2aa28bd9-3774-4518-9945-7f9277dd13ec" height="80%" width="80%" /> 
</p>
<br />


<p>
On the domain controller PC we will change the mainframe's record address to 8.8.8.8
</p> 
<p>
<img src="https://github.com/user-attachments/assets/44db04a3-2098-4185-8f05-e2e288435b2d" height="80%" width="80%" /> 
<img src="https://github.com/user-attachments/assets/097b0651-a5b3-44a2-a23d-e94ea24d21f0" height="80%" width="80%" /> 
</p>
<br />



<p>
Go back to the client PC and ping “mainframe” again. Observe that it still pings the old address.
</p> 
<p>
<img src="https://github.com/user-attachments/assets/f7952beb-9723-4f49-b814-fe71e89f4b8c" height="80%" width="80%" /> 
</p>
<br />



<p>
Observe the local DNS cache.
</p> 
<p>
<img src="https://github.com/user-attachments/assets/0f6fc4b8-b38b-4507-9570-c2c642561259" height="80%" width="80%" /> 
</p>
<br />




<p>
Flush the DNS cache.
</p> 
<p>
<img src="https://github.com/user-attachments/assets/8caf2088-00e2-4f13-af00-76817bc9fa45" height="80%" width="80%" /> 
</p>
<br />



<p>
Observe that the cache is empty.
</p> 
<p>
<img src="https://github.com/user-attachments/assets/d29b7d34-c21d-4ddb-b7d4-dccd9f6582fb" height="80%" width="80%" /> 
</p>
<br />



<p>
Attempt to ping "mainframe again. Observe the address of the new record is showing up.
</p>
<p>
<img src="https://github.com/user-attachments/assets/cc94dace-d803-41d7-813e-12a4f96a25bf" height="80%" width="80%" /> 
</p>
<br />


























