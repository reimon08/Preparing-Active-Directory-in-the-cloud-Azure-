<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>Overview of Deployment and Configuration Steps</h2>

- 🔧 Create a VM that will act as the Windows Server (Domain Controller)
- 💻 Create another VM with Windows 10 — this will act as the client machine
- 🌐 Join the Windows 10 VM to the domain that the Windows Server manages
- 👤 Log in to the Windows 10 client using domain credentials
- 🧪 This setup simulates a real environment with a domain controller and a connected client


<h2>Deployment and Configuration Steps</h2>

<h3>Create Resource Group</h3>

<p>We’re gonna start by creating a resource group called Active-Directory-Lab. This will hold all the resources we’ll be using for our Active Directory lab setup.</p>

<p>Choose the region closest to you and make sure to stick with that same region throughout the entire project to keep things consistent.</p>


https://github.com/user-attachments/assets/273afdfc-3094-4576-a587-4ee2bdf22238





