<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2> 

- To understand the roles of Admin and Agent
- To configure roles
- To configuere departments
- To configure teams
- To configure users 
- To configure SLA

<h2>Configuration Steps</h2>

To create a role 
- From the Admin panel, click Agents, then Roles, Add a new role.
- Chose a name for a new role
- Then click on Permissions and select the ones you want to grant in the three categories of Tickets, Tasks and Knowledgebase
- Save changes

![image](https://github.com/user-attachments/assets/2988b9a8-60d2-4b2a-a4a2-54571b4402da)

  
<p>

To create Departments
- From the Admin panel go to Agents, then click on Departments
- Add New Department. You will find different settings you can add and/or modify.
- Since you haven't configured the SLA's yet you can leave the default ones until you configure them.
-  After you fill out all the fields click on "create"

To create Teams
- Go to Admin panel, then Agents, click on Teams, then Add New Team.
- Fill out the blanks; You may name your teams according to different levels of support or specialty. Then click "Create a Team"

To Allow anyone to create tickets
- Go to Admin Panel, Settings, User Settings
- Be sure that Required Registration is unchecked.

  ![image](https://github.com/user-attachments/assets/a6d2f079-bde3-40c3-b862-f4c7afddce10)

  To configure Agents
  This will be the people that will resolve the tickets
  - In the Admin Panel go to Agents, Add New.
  - Fill in the blanks. Create a password. Notice that you have the option to ask Agents to change the password when they log in.
 
![image](https://github.com/user-attachments/assets/ea3a7f5e-0f6d-4297-b53d-9a1e9bfcbfbf)

- After you create the account click on Access. There you may assign the departments, Extended access, etc.
- Then you may set the Permissions and assign the Teams.
- To finalize click "Create".

To add Users
- From the Agent panel, go to Users, Add New.
- Fill in the blanks
- Click on "Add User"

To define SLA'S

Notice that in osTicket the SLA's are referred to the amount of time a ticket will be open, or better to say, how much time will take to solve it.  
- Go to Admin Panel, click Manage, then SLA. For the purpose of this tutorial we'll create 3 SLA's, We'll name each of them Sev-A,Sev-B and Sev-C. And we'll also assign a Grace Period and Schedule.
- From SLA, click on Add New SLA Plan. On Name write Sev-A, in Status select "Active", Grace Period type 1 (hour) and in Schedule select 24/7. "Add Plan".
- Then Add 2 more: Sev B (4 hours, 24 / 7) AND Sev C (8hours, business hours)
  
  ![image](https://github.com/user-attachments/assets/868f0079-59cc-453c-9de0-38c773003c78)

  To Create Help Topics
  These are the categories that the users will pick from when creating a ticket.
  - Go to Admin Panel, then click on "Manage", then on "Help Topics".
  - "Add New Help Topic"
  - In Topic type "Business Critical Outage". In Status select "Active". In Type select "Public"(for the rest of the topics the Status and the Type will be the same.
  - Parent Topic select: Report a Problem. Then click on Add Topic.
  - Following the same steps create the Help Topic "Computer Issues"
  - Add a third Help Topic and name it Equipment Request. In Status select "Active". In Type select "Public".
  - In Parent Topic select "General Inquiry". Then "add Topic".
  - Add another Help Topic. Name it "Password Reset" and as a Parent Topic select "Report a Problem".
  - Lastly add another Help Topic and name it "Other". Select "General Inquiry" as a Parent Topic.

    ![image](https://github.com/user-attachments/assets/db9ceb68-eac4-4ccd-bc60-93872b798b29)



