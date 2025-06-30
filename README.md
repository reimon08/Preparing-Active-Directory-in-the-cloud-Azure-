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

<h3>Create a Virtual Network</h3>

<p>Next, we’ll create a Virtual Network. While the VM setup wizard can create one for us automatically, we’re just gonna go ahead and create it ourselves to have more control over the setup.</p>

<p>We're going to name it Active-Directory-Vnet. Like I mentioned earlier, make sure to choose the same region you picked for the resource group; switching regions can cause issues later on, so it’s best to stay consistent from the start.</p>


https://github.com/user-attachments/assets/1b822789-2545-4ac3-b9f4-041b4b4512c0

<h3>Create the Virtual Machine for the Domain Controller</h3>

<p>Now we’re gonna create the VM that’ll act as our domain controller. For the name, we're gonna call it dc-1, for the image, pick Windows Server 2022 Datacenter. For the size, go with Standard_D2s_v3, it has 2 vCPUs and 8 GiB of memory, which is more than enough for this project. For the login, set the username to labuser and the password to Cyberlab123!.</p>

<p>Make sure to check all the licensing before you move forward</p>

<p>After that, just click "Next" through the tabs until you reach the Networking section. There, choose the Virtual Network we created earlier (Active-Directory-Vnet), leave everything else as default, then hit Review and Create to launch the VM.</p>


https://github.com/user-attachments/assets/68ab7123-e12f-4eb1-a2fe-ae5c15d83c91

<h3>Create Virtual Machine for Client-1</h3>

<p>Now we’re gonna create another VM and call it client-1. Make sure to place it in the same resource group as the domain controller. For the image, choose Windows 10 Pro 22H2, and for the size, go with the same one we used earlier — Standard_D2s_v3. Set the username to labuser and the password to Cyberlab123!. After that, just click "Next" through the tabs until you hit the Networking section, select the Virtual Network we created earlier (Active-Directory-Vnet), then hit Review and Create.</p>



https://github.com/user-attachments/assets/5eb92a6d-42fe-41f9-9bfc-cb7710752e0d














