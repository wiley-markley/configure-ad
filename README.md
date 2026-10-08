<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Configuring Active Directory Domain Services in Microsoft Azure</h1>
Deployed and configured an Active Directory domain controller and Windows 11 client in Microsoft Azure. Configured static networking, DNS, AD DS, and domain connectivity while troubleshooting Azure DNS configuration issues using Cloud Shell and PowerShell. <br />

<h2>Skills Demonstrated</h2>

- Azure VM deployment
- Windows Server administration
- Active Directory Domain Services
- DNS configuration/troubleshooting
- TCP/IP networking
- PowerShell
- Azure Cloud Shell
- Windows domain management
- Remote Desktop

This project demonstrates an understanding of several ideas and tools integral to entry-level IT. Deploying AD itself is important for a business setting that utilizes it for organizing its user database. Using cloud infrastructure to carry this out brings in another level of exposure to common IT tools, including VMs, OS, and RDP.

<h2>High-Level Deployment and Configuration Steps</h2>

- Deployed Windows Server and Windows 11 Azure VMs
- Configured a static private IP for the domain controller
- Configured the client VM to use the domain controller for DNS
- Troubleshot Azure DNS configuration using Cloud Shell
- Installed and configured AD DS
- Promoted the server to a domain controller
- Joined the Windows 11 client to the domain
- Validated DNS resolution and network connectivity

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
Used Azure Cloud Shell and PowerShell to update the client VM's DNS configuration to point to the domain controller's static private IP. Verified the resulting DNS configuration with ipconfig /all.
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
