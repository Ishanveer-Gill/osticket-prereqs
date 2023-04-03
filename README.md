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
- Web Platform Installer
- 

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
Install PHP Version 7.3.8 (or any other version if necessary, archives).

Install Microsoft Visual C++ 2009 Redistributable Package (if necessary).

Install PHP Manager 1.5.0 for IIS 10:
</p>
<br />

<p>
<img src="https://i.imgur.com/XhzCAtH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install osTicket v1.15.8

Download osTicket (Downloaded through lab files).

Extract and copy the “upload” folder INTO c:\inetpub\wwwroot:
</p>
<br />

<p>
<img src="https://i.imgur.com/lPM2vhi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/zymNVVS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
	Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”:
</p>
<p>
	<img src="https://i.imgur.com/pDikkgq.png" height="75%" width="100%" alt="rename to osTicket"/>
</p>
<br />
<br />
<h3 align="center">Reload IIS (Open IIS, Stop and Start the server)</h3>
<br />
<p>
	Go to sites -> Default -> osTicket:
</p>
<p>
	<img src="https://i.imgur.com/QeWNlG3.png" height="75%" width="100%" alt="default osTicket"/>
</p>
<p>
	On the right, click “Browse *:80”:
</p>
<p>
	<img src="https://i.imgur.com/3iXhNbi.png" height="75%" width="100%" alt="port 80"/>
</p>
<br />
<br />
<h3 align="center">Enable Extensions in IIS: Note that some extensions are not enabled</h3>
<br />
<p>
	Go back to IIS, sites -> Default -> osTicket.
</p>
<p>
	Double-click on PHP Manager:
</p>
<p>
	<img src="https://i.imgur.com/LFKo5Hs.png" height="75%" width="100%" alt="PHP Manager"/>
</p>
<p>
	Click “Enable or disable an extension”.
</p>
<p>
	Enable: php_imap.dll.
</p>
<p>
	Enable: php_intl.dll.
</p>
<p>
	Enable: php_opcache.dll:
</p>
<p>
	<img src="https://imgur.com/a/nrQo0kz" height="75%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />
<h3 align="center">Refresh the osTicket site in your browser, observe the changes</h3>
<br />
<p>
	<img src="https://i.imgur.com/6iSNd4H.png" height="75%" width="100%" alt="osTicket change"/>
</p>
<br />
<br />
<h3 align="center">Rename</h3>
<br />
<p>
	From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php.
</p>
<p>
	To: C:\inetpub\wwwroot\osTicket\include\ost-config.php:
</p>
<p>
	<img src="https://i.imgur.com/TEw71SD.png" height="75%" width="100%" alt="ost-config"/>
</p>
<br />
<br />
<h3 align="center">Assign Permissions: ost-config.php</h3>
<br />
<p>
	Disable inheritance -> Remove All:
</p>
<p>
	<img src="https://i.imgur.com/1QtRWEF.png" height="75%" width="100%" alt="disable inheritance"/>
</p>
<p>
	New Permissions -> Everyone -> All:
</p>
<p>
	<img src="https://i.imgur.com/YzsMXNX.png" height="75%" width="100%" alt="new permissions"/>
</p>
<p>
	<img src="https://i.imgur.com/k7x9yGR.png" height="75%" width="100%" alt="new permissions - all"/>
</p>
<br />
<br />
<h3 align="center">Finish setting up osTicket in the browser (click Continue)</h3>
<br />
<p>
	Name Helpdesk.
</p>
<p>
	Default email (receives email from customers):
</p>
<p>
	<img src="https://i.imgur.com/rvMvlNC.png" height="75%" width="100%" alt="continue osTicket setup"/>
</p>
<br />
<br />
<h3 align="center">Download and Install HeidiSQL</h3>
<br />
<p>
	<img src="https://i.imgur.com/AEg0b2P.png" height="75%" width="100%" alt="download HeidiSQL"/>
</p>
<p>
	Create a new session, root/Password1.
</p>
<p>
	Connect to the session:
</p>
<p>
	<img src="https://i.imgur.com/9t51ApR.png" height="75%" width="100%" alt="create sessions"/>
</p>
<p>
	Create a database called “osTicket”:
</p>
<p>
	<img src="https://i.imgur.com/vXzmQqg.png" height="75%" width="100%" alt="create database"/>
</p>
<br />
<br />
<h3 align="center">Finish setting up osTicket in the browser</h3>
<br />
<p>MySQL Database: osTicket</p>
<p>
	MySQL Username: root
</p>
<p>
	MySQL Password: Password1:
</p>
<p>
	<img src="https://i.imgur.com/akDyber.png" height="75%" width="100%" alt="setting up osTicket cont'd"/>
</p>
<p>Click “Install Now!”</p>
<p>Awesome, it should now be installed with no errors!</hp>
<p>
	<img src="https://i.imgur.com/J5omRoE.png" height="75%" width="100%" alt="installation complete"/>
</p>
<br />
<br />
<h3 align="center">Clean up</h3>
<br />
<p>
	Delete: C:\inetpub\wwwroot\osTicket\setup:
</p>
<p>
	<img src="https://i.imgur.com/eg0ZPG3.png" height="75%" width="100%" alt="clean up"/>
</p>
<p>
	Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php:
</p>
<p>
	<img src="https://i.imgur.com/n6k46XL.png" height="75%" width="100%" alt="permissions"/>
</p>
<br />
<br />
<h3 align="center">Login to the osTicket Admin Panel (http://localhost/osTicket/scp/login.php)</h3>
<br />
<p>
	<img src="https://i.imgur.com/zklvv8K.png" height="75%" width="100%" alt="admin panel"/>
</p>
<br />
<br />
<p>
	This is how you install osTicket. It is a great way to practice your own mock help desk. Thank you for anyone that has made it scrolling down this far.
</p>

