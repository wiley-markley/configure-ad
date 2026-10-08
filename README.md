<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Configuring Active Directory Domain Services in Microsoft Azure</h1>
Deployed and configured an Active Directory domain controller and Windows 11 client in Microsoft Azure. Configured static networking, DNS, AD DS, and domain connectivity while troubleshooting Azure DNS configuration issues using Cloud Shell and PowerShell. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- Cloud Shell
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2025
- Windows 11 (25H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Created Domain Controller
- Created Client VM
- Change DC NIC private IP to static
- Validate DNS traffic from Client VM to DC
- Promote dc-1 to Domain Controller
- Configured the client VM to use the domain controller as its DNS server

<h2>Deployment and Configuration Steps</h2>

<p>
<img width="512" height="197" alt="image" src="https://github.com/user-attachments/assets/c45650d7-9bf6-475b-a0f3-046f8956ce2a" />
</p>
<p>
Deployed an Azure VM using Windows Server OS to serve as a Domain Controller.
</p>
<br />

<p>
<img width="512" height="197" alt="image" src="https://github.com/user-attachments/assets/746ecf35-c196-4eeb-82ab-b9fb7a7ba9e2" />
</p>
<p>
Deployed a Windows 11 client VM in the same Azure region and virtual network as the domain controller.
</p>
<br />

<p>
<img width="512" height="183" alt="image" src="https://github.com/user-attachments/assets/4535c47b-5f3c-474d-9edf-3732490e5c36" />
</p>
<p>
Changed the domain controller's private IP allocation from dynamic to static to provide the client VM with a consistent DNS server address.
</p>
<br />

<p>
<img width="512" height="212" alt="image" src="https://github.com/user-attachments/assets/f86091cc-60c9-4c23-b7b7-4e9178c54149" />
</p>
<p>
Encountered an Azure DNS configuration issue when attempting to assign the domain controller's private IP as the client DNS server. Used Azure Cloud Shell to correct the DNS configuration and validated the resulting DNS assignment with ipconfig /all.
</p>
<br />

<p>
<img width="512" height="294" alt="image" src="https://github.com/user-attachments/assets/2b58ab08-8fd0-482b-b816-10380fa1dc51" />
</p>
<p>
Used Azure's Cloud Shell to override client-1's DNS server assignment. Then, used "ipconfig /all" in Windows 11 to validate that the DNS Server was then correct.
</p>
<br />

<p>
<img width="512" height="243" alt="image" src="https://github.com/user-attachments/assets/aed49b71-9c95-420e-b4f2-81465305d206" />
</p>
<p>
Used the ping command to dc-1's private IP from the Windows 11 VM to validate the connection.
</p>
<br />

<p>
<img width="768" height="538" alt="image" src="https://github.com/user-attachments/assets/a4d121f4-9c97-4082-87c5-44a1bdd96000" />
</p>
<p>
Promoted the Windows Server VM to a domain controller, configured AD DS, and joined the Windows 11 client to the domain. Verified domain membership, DNS resolution, and connectivity between the client and domain controller.
</p>
<br />
