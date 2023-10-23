<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Configure osTicket, post-installation](https://www.youtube.com)(Coming soon)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Configure Roles and Departments
- Configure Teams and Agents
- Configure Users
- Configure SLA
- Configure Help Topics

<h2>Configuration Steps</h2>

![image](https://github.com/nealzubin/post-install-config/assets/145185495/75ffaa43-4733-4d16-ad8b-7160718766e3)
![image](https://github.com/nealzubin/post-install-config/assets/145185495/c65fec36-debb-4243-b9c8-3001838be265)


<p>
Once you are logged into your VM, go to the URL for IT admins of osTicket: http://localhost/osTicket/scp/login.php
  
  * Enter the credentials you created last lab. The page should look like the one above.
  * AGENT PANEL VS ADMIN PANEL > the picture above is the agent panel as you can click on the link to the admin panel(shown below)
  * The ADMIN panel will allow you to set the roles/SLAs
  * Roles are permissions granted to agents per department they have access to.
  * Roles permissions for tickets include: assign, edit, close, link, etc
</p>
<br />


![image](https://github.com/nealzubin/post-install-config/assets/145185495/8a3f4b8a-92e2-4d14-accf-5564b6724708)




First role we will create is the "Supreme Admin". This role will essentially allow people to do anything in the osTicket. 

 * To do this we will go to admin panel > Agents > Roles
 * Click on "Add New Role" > Name the role "Supreme Admin"
 * Switch Tab to Permissions > Check all boxes on Tickets, Tasks, and Knowledgebase
 * Click "add role" > now we have a role with unlimited capability in osTicket
</p>
<br />

![image](https://github.com/nealzubin/post-install-config/assets/145185495/d85f7b40-a3cc-4f26-b692-3e41709b5920)
![image](https://github.com/nealzubin/post-install-config/assets/145185495/7dfe1bcf-144e-4819-86bf-1e13659357cd)
![image](https://github.com/nealzubin/post-install-config/assets/145185495/4a4380fe-7201-4e64-9316-336bab610f11)
![image](https://github.com/nealzubin/post-install-config/assets/145185495/d3b0f714-4d4f-47fe-b7f5-f334201901a7)
![image](https://github.com/nealzubin/post-install-config/assets/145185495/52e95d1a-68b1-438c-97a2-8bcc7ac120a5)




<p>

Since tickets are routed through departments in the helpdesk, there are many settings that can be set for each department

 * Each of the deparments might have differing SLAs
 * To configure departments: Go to Admin panel > Agents > Departments
 * Click "Add New Department"
 * Name the department. ex: "System Administrators"
 * We will keep the SLAs as default for now, but this can be set as needed
 * We will keep all other options here as default for this lab
 * click "Create Dept"
</p>


![image](https://github.com/nealzubin/post-install-config/assets/145185495/dc3f2c29-9b38-4dea-8627-9b71d9cd86b0)
![image](https://github.com/nealzubin/post-install-config/assets/145185495/83c5da20-ced4-47f8-8ac9-6dbf67347af7)
![image](https://github.com/nealzubin/post-install-config/assets/145185495/80c8af74-1ffa-46c7-b05b-3453e46c3cc4)

<br />




<p>

We are going to configure teams next. Teams allow you to pull agents from different departments and orgranize them to handle a specific issue or user via a help topic or ticket filter

 * To configure teams: Go to Admin panel > Agents > Teams
 * Click "Add New Team"
 * Name the team: Level II support, in an organization this could be the subject matter experts(SMEs)
 * Switch to the members tab > add members who belong to the team
 * We will keep all other options here as default for this lab
 * click "Create team"
</p>


![image](https://github.com/nealzubin/post-install-config/assets/145185495/5576c194-af58-441c-8cc3-6c215edc3e14)
![image](https://github.com/nealzubin/post-install-config/assets/145185495/dd376926-a199-42be-9aa5-8fb2e60a9952)
![image](https://github.com/nealzubin/post-install-config/assets/145185495/4a878db8-8de0-4107-b331-08ad9f44aed9)






<p>

We are going to allow anyone to create tickets

 * Admin Panel -> Settings -> User Settings
 * uncheck Registration Required: Require registration and login to create tickets 

</p>


![image](https://github.com/nealzubin/post-install-config/assets/145185495/1eca9a3d-3b12-4514-8fd2-fc55ff998c4a)






<p>

Next, we are going to create some agents. Agents are given access to the help desk with the intent to respond and resolve the tickets

 * Admin Panel -> Agents -> Add New
 * Set password just for this lab, in practice it is not recommended to keep one password for all agents
 * Go to access tab > select primary department
 * Go to teams tab > add to level II support
 * click Create

</p>


![image](https://github.com/nealzubin/post-install-config/assets/145185495/be728842-6e52-4257-b7ca-fd72744bf62e)
![image](https://github.com/nealzubin/post-install-config/assets/145185495/74dd4e66-8edb-420e-906b-0e81082196d9)
![image](https://github.com/nealzubin/post-install-config/assets/145185495/ef61ae02-8ba7-4aba-a0f9-3f2da1bfc2e6)





<p>

Next, we are going to create users. We will need to switch to the agent panel to do this. 

 * Agent Panel -> Users -> Add User
 * Set password just for this lab, in practice it is not recommended to keep one password for all agents
 * click Create

</p>


![image](https://github.com/nealzubin/post-install-config/assets/145185495/f1162065-f3d7-4fd8-93ed-20a8c19783cf)
![image](https://github.com/nealzubin/post-install-config/assets/145185495/8b218812-122c-4e2e-8ed5-6e771c536bc2)
![image](https://github.com/nealzubin/post-install-config/assets/145185495/669c515c-0865-457b-abf9-93174208d1c3)





<p>

We will now configure SLAs. The purpose of the SLA is to provide a length of time in which tickets are expected to be resolved. We will need to go back to the admin panel for this.  

 * Admin Panel -> Manage -> SLA
 * Sev-A (1 hour, 24/7)
 * Sev-B (4 hours, 24/7)
 * Sev-C (8 hours, business hours)

</p>



![image](https://github.com/nealzubin/post-install-config/assets/145185495/6fc6b16e-0c4e-41f3-8960-0da7bea23d94)
![image](https://github.com/nealzubin/post-install-config/assets/145185495/6342af64-3626-43a8-ab0c-d658c5935068)
![image](https://github.com/nealzubin/post-install-config/assets/145185495/f3bc24b9-a21c-4fdc-afca-750456687cfb)
![image](https://github.com/nealzubin/post-install-config/assets/145185495/aabd6022-7ffd-4d31-b32f-c0d16b4c8c68)






<p>

We will now configure Help Topics. Help topics help streamline the end-user experience. 

 * Admin Panel -> Manage -> Help Topics
 * Business Critical Outage
 * Personal Computer Issues
 * Equipment Request
 * Password Reset
   
</p>


![image](https://github.com/nealzubin/post-install-config/assets/145185495/68851e31-47ff-4418-bcd4-96bf2b8d9db0)
![image](https://github.com/nealzubin/post-install-config/assets/145185495/a1252e85-b062-4bff-b0d0-557e33c89e0b)




<p>

We are at the end of this lab. We will use what we configured in this lab in the next section. 
   
</p>






