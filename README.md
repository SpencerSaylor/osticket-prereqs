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

- Item 1
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/eAUNKvn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1. First we need to enable IIS (Internet Information Services) with CGI (Common Gateway Interface). This will allow us to host our own server for osTicket. The steps taken to do this as follows:
<ol>
	<li>Press the Windows Key + R and type 'Control" to bring up the Control panel.</li>
	<li>From there, select uninstall program --> Turn windows features on or off</li>
	<li>Scroll and select and IIS --> World Wide Web Services --> Application Development features and select CGI.</li>
</ol>
</p>
<br />

<p>
2. From our install folder, we'll need to install:
<ol>
	<li>PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)</li>
	<li>Rewrite Module (rewrite_amd64_en-US.msi)</li>
	<li>VC_redist.x86.exe.</li>
</ol>
</p>
<br />

<p>
<img src="https://i.imgur.com/9ojIjAs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
3. Create a folder in the directory C:\PHP and from the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder
</p>
<br />

<p>
4. We will then install MySQL 5.5.62 (mysql-5.5.62-win32.msi) and then do the following setup:
<ol>
	<li>Typical Setup -></li> <p><img src="https://i.imgur.com/hNwJ3n2.png" height="50%" width="50%" alt="Typical Setup"/></p>
	<li>Launch Configuration Wizard (after install) -></li>
 	<li>Standard Configuration -></li><p><img src="https://i.imgur.com/RJ5JbXS.png" height="50%" width="50%" alt="Standard Config"/></p>
	<li>Username: root</li>
	<li>Password: root</li><P><img src="https://i.imgur.com/eGgLf85.png" height="50%" width="50%" alt="Standard Config"/></P> 
	It is a terrible idea to put the username and pass as root, but as a lab it'll be ok.
</ol>
</p>
<br />

<p>
	5. Open IIS as admin
</p>
<br />

<p>
	6. Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)
</p>
<br />

<p>
	7. Reload IIS (Open IIS, Stop and Start the server)
</p>
<br />

<p>
	8. Install osTicket v1.15.8
 <ul>
	 <li>From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”</li>
	 <li>Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”</li>
 </ul>

</p>
<br />

<p>
	9. Reload IIS (Open IIS, Stop and Start the server)
</p>
<br />

<p>
	10. From the IIS Manager, Go to sites -> Default -> osTicket
 <ul>
	 <li>On the right, click “Browse *:80”</li>
 </ul>

</p>
<br />
