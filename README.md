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

<h2>Prerequisites</h2>

In order to observe osTicket lifecycles, osTicket must have been already installed and have post-installation configurations.

* Prerequisites and Installation Tutorial: https://github.com/darinnstathos/osticket-prereqs.git
* Post-Installation Configurations Tutorial: https://github.com/darinnstathos/post-install-config.git

<h2>Lifecycle Stages</h2>

<h3>🟢 Intake (All Tickets)</h3>

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

<img src="https://i.imgur.com/pkYxnl0.png" height="80%" width="80%" alt="Creating a Ticket within osTicket"/>
<img src="https://i.imgur.com/6sFmDTZ.png" height="80%" width="80%" alt="Karens Ticket"/>

<br>

<p>Now, we're going to pretend we're Ken from the Accounting Department and create another ticket for a different issue.</p>

1. Select ‘Open a New Ticket'
2. Write in the fields provided: (for practice sake)

- Email: ken@osticket.com
- Name: Ken Ken
- Help Topic: 'Personal Computer Issues'
- Extra information: ‘Ever since the upgrade last night, nobody in accounting has been able to use Adobe Reader’ 

4. Select "Create Ticket"

<img src="https://i.imgur.com/xyDaxiO.png" height="80%" width="80%" alt="Kens Ticket"/>

<br>

<h3>🔵 Troubleshooting: Giving Jane Doe Permissions</h3>

<p>Before continuing with the tutorial, we need to grant Jane Doe 'Supreme Admin' access. This will help us continue the rest of the project.</p>

1. Navigate to the admin link: http://localhost/osTicket/scp/login.php
2. Log in as Jane Doe: username: jane.doe / Password1
3. When we login, we can see the tickets aren’t showing up so we’re going to troubleshoot by logging in as the admin and checking Jane’s permissions

<img src="https://i.imgur.com/EBkizSI.png" height="80%" width="80%" alt="No Tickets appearing"/>

4. Navigate back to the admin login link: Login as 'Supreme Admin': (example: darin_admin)
5. When we log in, we can see the tickets appear via the Agent Panel as Supreme Admin
6. Select 'Admin Panel' > click ‘Agents’ > click ‘Jane Doe' 

<img src="https://i.imgur.com/DIzf2fX.png" height="80%" width="80%" alt="No Tickets appearing"/>
<img src="https://i.imgur.com/DrXitAx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

7. Select ‘Access’ > Under Extended Access: ‘Support’ for Department > click ‘Add’ > ‘Supreme Admin’ for Role > ‘Save Changes’
8. Login with the admin link for Jane Doe again: 

- username: jane.doe / Password1

9. When we login, we can now see the tickets. That means, in this case, in order to work on Tickets, someone must be assigned specifically to the Support Department along with a role that will allow them to work on tickets 
 
<img src="https://i.imgur.com/44W51wa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/nxO9mXF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


<br>

<h2>Mobile Banking Ticket</h2>

<h3>🟢 Assignment & Communication</h3>

<p>We’re going to go through these tickets right now and edit them/tweak them. Right now, it appears that the tickets all have ‘Normal’ priority.</p>

1. Select the ticket ‘Entire Mobile Online Banking is Down’ ticket
2. Select ‘Priority’ > Set Priority Level to ‘Emergency’ (since this is a business impacting event) > Select ‘Update’
3. We can assign to an agent as well: select ‘Assigned To’ > select assignee ‘Jane Doe’ > select ‘Assign’
4. Since this is severe business-impacting event, we want to alter the SLA accordingly: select ‘SLA Plan’ > set SLA to ‘SEV-A’
5. If the entire system is down, it might be beyond the scope of the Help Desk: select ‘Department’ > transfer the ticket from ‘Support’ to ‘System Administrators’
6. We can see the history of edits/things that have been changed so far and the thread of messages created as part of effective communication
7. If we exit out and back into the panel, we can see some of the changes we’ve made: “Emergency” and “Assigned to Jane Doe”

<img src="https://i.imgur.com/qnwOBvv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/NrwgiW7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/C8EztbP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/Cr78Mub.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br>

<h3>🟢 Working the Issue</h3>

<p>We can go back inside of the ticket and communicate that the ticket was worked on/resolved.</p>

<p>In this example: "Jerry from Systems Engineering found and corrected a failed load balancer. Mobile banking should be back up." 
  
<img src="https://i.imgur.com/8ILZffg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  
<br>
  
<h3>🟢 Resolution</h3>

1. The status of the ticket was changed to ‘Closed’ (since Jerry from Systems Engineering resolved the issue)
2. When we navigate back to the Tickets portal and select ‘Closed’, we can see the ticket was moved there. 

<img src="https://i.imgur.com/oy0O0ML.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<br>

<h2>Accounting Department Adobe Ticket</h2>

<h3>🟢 Assignment & Creation</h3>

1. Navigate back to ‘Tickets’ portal & select ‘Entire Accounting Dept Adobe Reader Not Working’ ticket
2. Open the ticket and work through it/give it proper assignments:

- Priority: High

<p>It’s not as crucial as mobile banking being down but if the entire accounting dept is experiencing difficulties, that has a relatively high impact.</p>

- SLA: SEV-B
- Assignee: John

<p>We want to assign it to someone so that the delegated person can start working and reach out/communicate with the accounting department.</p>

3. In the ticket thread, John and Ken can start collaborating:“Re-assigned to SEV-B, reached out to John for a warm hand off”

<img src="https://i.imgur.com/MbIiEC0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


<br>

<h3>🟢 Working the Issue</h3>

<p>Since this is John’s ticket now, we’re going to re-login to the Admin portal as John in order to start working on the ticket.</p>

1. Login as John: username: john.doe / Password1
2. We can see the ticket appear on John's dashboard
3. John can look inside the ticket and see the communication that happened with Jane Doe: We can see it was reassigned as a SEV-B issue. John can see the problem is that Adobe Reader not working. Since it’s a SEV-B, John can conclude he was 4 hours to fix this due to SLA ruling. 
4. John can write in the Ticket Thread to communicate how we plans to solve the issue: 

- Example: “Rolled back version of Adobe Reader to previous version allowing the accounting department to work. 

In the meantime, I will research why the new version doesn't work on the accounting department's hardware”

<img src="https://i.imgur.com/bG366fp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/zpEuQhL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/XEjW70H.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<br>

<h3>🟢 Resolution</h3>

1. For this example, John found the issue and now he’ll communicate in the Ticket Thread:

<p>“Figured out the problem, re-upgraded everyone. Adobe Reader on the accounting department's device should be working”</p>

2. Mark the ticket as ‘Resolved’
3. Navigate to 'Tickets' > 'Closed' > The ticket has moved here 

<img src="https://i.imgur.com/Q76kRCs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/7zYRnzD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>




