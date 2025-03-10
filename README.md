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

- A-Record exercise
- Local DNS cache exercise
- CNAME record exercise

<h2>Deployment and Configuration Steps</h2>

**A-Record exercise**
<p>
After logging into both the domain controller pc and the client pc as the administrator, ping "mainframe" and observe the failure.
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






























