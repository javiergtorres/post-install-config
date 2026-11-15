# post-install-config

<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket as an Admin.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 11</b> 

<h2>Post-Install Configuration Objectives</h2>

- Configure Roles (for grouping permissions)
- Configure Departments (Ticket Visibility, Help Desk vs SysAdmins, vs Networking)
- Configure Teams
- Allow anyone to create tickets
- Configure Agents (workers)
- Configure Users (customers)
- Configure SLA
- Configure Help Topics (For when users create a ticket)

<h2>Configuration Steps</h2>

<p>
<img width="1906" height="859" alt="screenshot-microsoftazure-osticket-vm" src="https://github.com/user-attachments/assets/0416999a-ee6f-4135-acfc-f025093d8ef8" />

</p>
<p>
First thing, I created a Windows 11 virtual machine in Microsoft Azure. I'll need the public IP address, username, and password of the virtual machine so I can remote desktop in to the virtual machine. You can see the public IP address in the photo. 
</p>
<br />

<p>
<img width="1915" height="1078" alt="screenshot-garudalinux-rdp" src="https://github.com/user-attachments/assets/c072daaa-5e8e-4f68-94f4-d66913a8015e" />

</p>
<p>
The software I'm using on my laptop is Garuda Linux. Here you can see I'm using Remmina, a Remote Desktop Protocol application, one of the main options for using RDP on Linux. All I need is to punch in the public IP address of the virtual machine, username, and password in the correct fields.  From here I'll connect to the Windows 11 virtual machine by pressing the connect button.
</p>
<br />

<p>
<img width="1856" height="1027" alt="screenshot-osticket-adminloginscreen" src="https://github.com/user-attachments/assets/4425dd80-5518-498a-a02f-64705776f6f2" />

</p>

<p>
Here I'm on the osTicket admin login screen. I'll type the username and password and login.
</p>
<br />

<p>
<img width="1826" height="1014" alt="screenshot-osTicket-agents-to-roles-configuration" src="https://github.com/user-attachments/assets/09b2df0a-d8ae-43ee-81b4-130095393ba1" />
</p>

<p>
  From here I'll click the "Agents" button, then I'll click the "Roles" button. I'll create a "Supreme Admin" role.
</p>

<p>
  <img width="1826" height="1014" alt="screenshot-adding-new-role" src="https://github.com/user-attachments/assets/081af633-3a33-4001-8c78-76440cb30b3d" />

</p>

<p>
  From here, I'm going to click "add new role"
</p>

<p>
  <img width="1811" height="1011" alt="screenshot-creating-supremeadmin" src="https://github.com/user-attachments/assets/92324b73-fa15-4e6d-bfe5-f9f8f7d7b43d" />

</p>

<p>
  Here I'm creating a "Supreme Admin" role, and I'm going to give it all permissions to do everything. 
</p>

<p>
  <img width="1817" height="1004" alt="screenshot-giving-all-permissions-to-supremeadmin" src="https://github.com/user-attachments/assets/806444e6-e584-4766-8852-5a359448ab59" />

</p>

<p>
  Here I clicked "Permissions" , and under "Tickets", "Tasks", and "Knowledgebase" I'm going to check every box then click "Add Role". Then the "Supreme Admin" role will be created. After that I'll create a department called "SysAdmins".
</p>

<p>
  <img width="1824" height="1008" alt="screenshot-adding-sysadmin-department" src="https://github.com/user-attachments/assets/10e577c1-99ab-4ce4-8f4c-806bfbaa29d5" />

</p>
