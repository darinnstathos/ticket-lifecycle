<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Ticket Lifecycle: Intake Through Resolution</h1>
This tutorial outlines the lifecycle of a ticket from intake to resolution within the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Ticket Lifecycle Stages</h2>

- Intake
- Assignment and Communication
- Working the Issue
- Resolution

<h2>Lifecycle Stages</h2>

<h3>Intake (All Tickets)</h3>

<p>We’re going to act as end-users in order to create some tickets and acquire a better understanding on how the osTicket platform operates.</p>

<p>In this example, we're going to pretend we're Karen, the manager that oversees Mobile Banking:</p>
  
1. Navigate to the end-user URL: http://localhost/osTicket/
2. Select “Open a Ticket”
3. Write in the fields provided: (for practice sake)

- Email: karen@osticket.com
- Name: Karen Karen
- Help Topic [we created these earlier]: Business Critical Outage
- Issue Summary: “Entire mobile banking system is down”
- Extra Information: “Customers are reporting that they're getting a 404 error when browsing to online banking”

4. Select "Create Ticket"

<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<br>

<p>Now, we're going to pretend we're Ken from the Accounting Department and create another ticket for a different issue.</p>

1. Select ‘Open a New Ticket'
2. Write in the fields provided: (for practice sake)

- Email: ken@osticket.com
- Name: Ken Ken
- Help Topic: 'Personal Computer Issues'
- Extra information: ‘Ever since the upgrade last night, nobody in accounting has been able to use Adobe Reader’ 

4. Select "Create Ticket"

<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<br>

<h3>Troubleshooting: Giving Jane Doe Permissions</h3>

<p>Before continuing with the tutorial, we need to grant Jane Doe 'Supreme Admin' access. This will help us continue the rest of the project.</p>

1. Navigate to the admin link: http://localhost/osTicket/scp/login.php
2. Log in as Jane Doe: username: jane.doe / Password1
3. When we login, we can see the tickets aren’t showing up so we’re going to troubleshoot by logging in as the admin and checking Jane’s permissions
4. Navigate back to the admin login link: Login as 'Supreme Admin': (example: darin_admin)
5. When we log in, we can see the tickets appear via the Agent Panel as Supreme Admin
6. Select 'Admin Panel' > click ‘Agents’ > click ‘Jane Doe' 
7. Select ‘Access’ > Under Extended Access: ‘Support’ for Department > click ‘Add’ > ‘Supreme Admin’ for Role > ‘Save Changes’
8. Login with the admin link for Jane Doe again: 

- username: jane.doe / Password1

9. When we login, we can now see the tickets. That means, in this case, in order to work on Tickets, someone must be assigned specifically to the Support Department along with a role that will allow them to work on tickets 
 
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<br>

<h3>Assignment & Communication: Mobile Banking Ticket</h3>








