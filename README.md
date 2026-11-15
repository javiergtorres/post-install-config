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
  From here I'll click the "Agents" button, then I'll click the "Roles" button. I'll create a "Supreme Admin" role. The point of Roles is for grouping permissions.
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
  Here I clicked "Permissions" , and under "Tickets", "Tasks", and "Knowledgebase" I'm going to check every box then click "Add Role". Then the "Supreme Admin" role will be created. 
</p>

<p>
  <img width="1807" height="1038" alt="screenshot-supremeadmin-role-created" src="https://github.com/user-attachments/assets/7eb86877-8414-4496-9fe8-4e31aa6edf99" />

</p>

<p>
  "Supreme Admin" role has been created.
</p>

<p>
  <img width="1824" height="1008" alt="screenshot-adding-sysadmin-department" src="https://github.com/user-attachments/assets/10e577c1-99ab-4ce4-8f4c-806bfbaa29d5" />

</p>

<p>
  Here I'm on the Departments page, and I'll click "Add New Department". I'll be creating a new department called "SysAdmins". Departments will be for ticket visibility, different departments will be able to view specific tickets designated for specific departments.
</p>

<p>
  <img width="1878" height="1043" alt="screenshot-creating-sysadminsdepartment" src="https://github.com/user-attachments/assets/5d2de449-5d4f-4934-94bc-6d1fcc96f7e7" />

</p>

<p>
  <img width="1861" height="1036" alt="screenshot-creating-sysadminsdepartment-pt2" src="https://github.com/user-attachments/assets/8b8de0ff-9412-4d9c-af8b-9051fe396c2e" />

</p>

<p>
  Here you can see I'm creating a "SysAdmins" department, making sure that in the "Parent" section, it's listed as a "Top Level Department" so the department will be able to see all tickets. For now, that's all I'll configure, then I'll hit "Create Dept" at the bottom of the screen.
</p>

<p>
  <img width="1854" height="1043" alt="screenshot-sysadminsdepartment-created" src="https://github.com/user-attachments/assets/9b519d0c-48ec-49fd-9590-727fbc3d7e28" />

</p>

<p>
  "SysAdmins" department has been created.
</p>

<P>
  <img width="1827" height="1047" alt="screenshot-creating-onlinebanking-team" src="https://github.com/user-attachments/assets/929bf863-83d0-4d7d-a135-05e191aaa078" />

</P>

<p>
  Now I'm going to create an "Online Banking" team. The point of teams is if you want to create a group of people who are all from different departments. Under the "Agents" tab, click "Teams", then click "Add New Team".
</p>

<p>
  <img width="1849" height="1042" alt="screenshot-actually creating-onlinebanking-team" src="https://github.com/user-attachments/assets/00ab0f31-0d6d-4330-b92c-f74ce2a3f752" />

</p>

<p>
  Here I'm creating the "Online Banking" team, from here I"ll click "Create Team".
</p>

<p>
  <img width="1836" height="1047" alt="screenshot-onlinebankingteam-created" src="https://github.com/user-attachments/assets/c7caeb8d-d092-40d4-84d3-1abe86930faf" />

</p>

<p>
  "Online Banking" team has been created.
</p>

<p>
  <img width="1844" height="1045" alt="screenshot-settings-usersettings" src="https://github.com/user-attachments/assets/a759b1ba-2bb5-42e3-a24c-0a2cb173d98e" />

</p>

<p>
  Now I'm going to adjust the settings so that any End User can create a ticket, without the need to have an account. I'll go to "Settings", then "User" settings. Where it says, "Registration Required", I want to make sure that box is left unchecked.
</p>

<p>
  <img width="1825" height="1051" alt="screenshot-addnewagents-panel" src="https://github.com/user-attachments/assets/c8c73f17-2cd1-4e4a-bc8c-70d0914215ff" />

</p>

<p>
  Next, I'm going to create two "Agents". Agents, for example, are when a company hires new employees so Agent accounts get created for new hires. I'll be creating, "Jane (Dept: SysAdmins)" and "John (Dept: Support)". In the Admin panel, I go to "Agents", then "Add New Agent". The following screenshots will show me creating both "Agents" and permissions I have decided they'll have.
</p>

<p>
  <img width="1835" height="1040" alt="janedoe" src="https://github.com/user-attachments/assets/e9013f31-c279-4427-a469-8a1a2e05b470" />

</p>

<p>
  <img width="1834" height="1045" alt="creatingjane-1" src="https://github.com/user-attachments/assets/ab13d348-9502-46f3-973d-32453b080afc" />

</p>

<p>
  <img width="1833" height="1046" alt="creatingjane-2" src="https://github.com/user-attachments/assets/b44d11f1-0893-40d2-a376-29f9a5275e85" />

</p>

<p>
  <img width="1837" height="1046" alt="creatingjane-3" src="https://github.com/user-attachments/assets/6345da2c-68f5-4ce9-90b2-6f52b455b214" />

</p>

<p>
  <img width="1846" height="1044" alt="creatingjohn-1" src="https://github.com/user-attachments/assets/832f1829-aa7a-41ee-a6d3-89374871a4ee" />

</p>

<p>
  <img width="1844" height="1041" alt="creatingjohn-2" src="https://github.com/user-attachments/assets/1c86e04c-d2a6-4c3e-b57e-0d059a4f9198" />

</p>

<p>
  <img width="1848" height="1042" alt="bothjaneandjohncreated" src="https://github.com/user-attachments/assets/571dff8c-c32c-4463-9d17-8fb5ffe9bb8f" />

</p>

<p>
  Here are both "Jane" and "John" Agent accounts created.
</p>

<p>
  <img width="1837" height="1041" alt="creatinguser-karen" src="https://github.com/user-attachments/assets/abcacc01-b4cb-4f29-9f89-a86d4d193860" />

</p>

<p>
  Next, I'll add a "User", I'll call her "Karen". For that I go to the "Agent Panel" near the top of the screen. Then I click "Users", after that click "Add User".
</p>

<p>
  <img width="1848" height="1045" alt="karenflores-user-creating" src="https://github.com/user-attachments/assets/821faf8a-2dfe-4e1d-afd8-b6e9df2e674f" />

</p>

<p>
  Here I'm creating the user account, then I'll click "Add User".
</p>

<p>
  <img width="1847" height="1038" alt="karen-hasbeencreated" src="https://github.com/user-attachments/assets/3e544610-bdcb-4aa3-9f44-a4c9d3b4c15e" />

</p>

<p>
  User account for Karen has been created.
</p>

<p>
  <img width="1848" height="1046" alt="manage-then-SLA" src="https://github.com/user-attachments/assets/ea55cc51-044c-4a79-ab4d-6fcc88c5c7bc" />

</p>

<p>
  Now I'm going to configure SLAs, which basically is how much time you have to do some specific task. Whether that's responding to a ticket, or completing a ticket, etc. For that, I'll go back to the Admin panel at the top of the screen. Then I click the "Manage" button, then "SLA". Then I click "Add new SLA plan".
</p>

<p>
  <img width="1848" height="1046" alt="manage-then-SLA" src="https://github.com/user-attachments/assets/e911fb40-5e0f-424e-8eb9-91374fe4cd06" />

</p>

<p>
  I'm going to create three SLAs:

  Sev-A (Grace Period: 1 hour, Schedule: 24/7)

  
Sev-B (Grace Period: 4 hours, Schedule: 24/7)


Sev-C (Grace Period: 8 hours, Business Hours)
--------------------------------------------------------------------------------------------------------------------


Sev-A: for a really bad problem that affects a business in a really bad way and must be fixed ASAP!


Sev-B: for a slightly less bad problem


Sev-C: for a problem that really isn't that bad
</p>
