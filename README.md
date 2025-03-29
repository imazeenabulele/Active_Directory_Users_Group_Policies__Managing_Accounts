# Active_Directory_Users_Group_Policies__Managing_Accounts

<p align="center">
<img src="https://i.imgur.com/dD3HdHo.jpeg" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Creating Users, Group Policies and Managing Accounts with Active Directory in Azure</h1>
This section will show the setting up of non-administrative users   .<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>
- Setup up Remote Desktop for non-admin users on Client-1<br />
- Create a bunch of additonal users and attempt to log into clients-1 with on of the users

<h2>Deployment and Configuration Steps</h2>

<p>
Firstly, we'll log into Client-1 as jane_admin since clinet-1 has not been joined to the domain where jane has adminstrative priviledges.<br /><br />
Once logged in, right click the start menu > Click "system" > "Remote Desktop" > "select users that can remotely can access this PC" > "Add" > type Domain Users > Click Ok. By doing this, all domain users by default would be allowed to log into the VM.  This also means you can log into Client-1 as non-administrative user
</p>

<p>
<img src="https://i.imgur.com/4VVOfHM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br /><br />

<p>
Now, we'll log into DC-1 the users would be created. Open Powershell ISE as an administrator, create a new file and input a script that would create users. The script as seen below will create 1000 users with random names
</p>

<p>
<img src="https://i.imgur.com/CnqVfHk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br /><br />

<p>
Once the run buttin is clicked, the user accounts will be created. 
</p>

<p>
<img src="https://i.imgur.com/5BBrCqY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br /><br />


<p>
Now the users have been created, we'll pick any user account and attempt to log into it. It should work because these users are members of the domain. Let's go with "jaca.nun" 
</p>

<p>
<img src="https://i.imgur.com/ogJ8zNW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br /><br />


<p>
Before we log in, let's checkout the details of this user account
</p>

<p>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br /><br />

