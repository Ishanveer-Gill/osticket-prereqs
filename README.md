<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Machine
- osTicket Installation files
- Heidi SQL

<h2>Installation Steps</h2>
First we will create a Virtual Machine using Microsoft Azure portal. A Virual Machine is a remote computer which you can access by using the Remote Desktop Connection app. It is best to use a Virtual Machine to protect our physical machine in case something breaks. First we will create a resource group and title it "osTicket". Afterwards create a Virtual Machine that has 2-4 CPUs. 
<p>
<img src="https://i.imgur.com/qsISkUj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we will connect to our Virtual Machine using Remote Desktop Connection app. 
</p>
<br />
<p>
<img src="https://i.imgur.com/i4A433w.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install/Enable IIS in Windows
</p>
<br />

<p>
<img src="https://i.imgur.com/4hznclZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install Web Platform Installer
</p>
<br />

<p>
<img src="https://i.imgur.com/eOFvvpA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open after installation
</p>
<br />

<p>
<img src="https://i.imgur.com/zWm3VRc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we will add MYSQL 5.5 (creditals are later asked to be created)
  
  (Default Username: Root)
  
  (Password: Password1)
</p>
<br />

<p>
<img src="https://i.imgur.com/QZ04EH4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Add all simple versions of x86 PHP up until 7.3:
</p>
<br />

<p>
<img src="https://i.imgur.com/Pnaf84m.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Fix any failures if required.

Install PHP Version 7.3.8 (or any other version if necessary, archives).

Install Microsoft Visual C++ 2009 Redistributable Package (if necessary).

Install PHP Manager 1.5.0 for IIS 10:
</p>
<br />

<p>
<img src="https://i.imgur.com/XhzCAtH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/QZ04EH4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
