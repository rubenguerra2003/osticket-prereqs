<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Enable IIS and CGI
- Install PHP manager
- Install rewrite amd
- Install mysql and setup a username and password
- Install c++ redistributable
- Configure permissions and install osTicket

<h2>Installation Steps</h2>

Now we need to install / Enable IIS in Windows. Go to your Search Bar > Type "Control Panel" > Click "Programs" > "Turn Windows features on or off" > Scroll down to "Internet Information Services (IIS).</h3>
<br />
<p>
  
![osticketlab snip](https://github.com/user-attachments/assets/595fbddc-ad2f-49bb-be7e-c1d23b0eab45)
</p>
<br />
<br />
<h3 align="center">Once clicked, find the "Internet Information Services" expand it and then expand the "World Wide Web" tab. Afterward, expand the application Developer tab. Finally check the "CGI" button & press Ok. You will need CGI to download the PHP Manager. The PHP manager is a back-end web programming language that allows osTicket to run off a web browser.</h3>
<br />
<p>
  
![turn cgi on](https://github.com/user-attachments/assets/848cc61c-1dfa-4267-a72e-6dd53a46b42d)

</p>
<br />
<h3 align="center">Install PHP Manager</h3>
<br />
<p>
<h3 align="center">Download the PHP manager file, and agree with all the terms. We've now downloaded the PHP manager into our operating system.</h3>
<p>
 
</p>
<br/>
<h3 align="center">Install Rewrite Module</h3>
<br />
<p>
<h3 align="center">Download the Rewrite Module file, agree with all the terms and it should now be installed onto the Computer.</h3>
<p>
	
 ![rewrite](https://github.com/user-attachments/assets/4734f0d7-881a-4113-b8fc-22649c55d35d)
 
</p>
<br/>
<h3 align="center">CREATE DIRECTORY C:\PHP</h3>
<br />
<p>
<h3 align="center"> Open File Explorer, type, "C:\" in the search bar, Right-click and create a new folder called, "PHP". Download php-7.3.8-nts-Win32-VC15-x86.zip from<a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> Files You Need to Download</a>, Extract it by going to where you download the file, Right-click the PHP 7.3.8 file and press extract to the PHP Folder you just created.
</h3>
<p>
  
  ![osticketlab snip transfer extract to c php](https://github.com/user-attachments/assets/c464a1ba-7e18-4ba8-a20a-e007cd9e76ea)

</p>
<br/>
<h3 align="center">VC_REDIST DOWNLOAD</h3>
<br/>
<h3 align="center"> Download and install VC_Redist, Agree with any terms and agreements and finish installing.
</h3>
<p>
  
 ![osticketlab install vcredist](https://github.com/user-attachments/assets/d2f73171-b1ac-4568-9d90-37059db283c8)


</p>
<br/>
<h3 align="center">DOWNLOAD MySQL </h3>
<h3 align="center"> Download and install MySQL, Agree with any terms and agreements up until you get to the password portion. Here you can create a username and password for the database that you'll be using to store the Ticket Information used in osTicket. 
</h3>
<p>
  
![osticketlab install mysql](https://github.com/user-attachments/assets/09f9fe97-0e72-4bd2-86c5-c98a5e3a2ce3)
![osticketlab set sql password](https://github.com/user-attachments/assets/a2c0850a-da98-4856-9f4e-c4b225793116)

<br/>
</p>
<br/>
<h3 align="center">Install osTicket v1.15.8</h3>
<br />
<p>
  Download osTicket (download from within lab files: link).
</p>
<p>
	Extract and copy the “upload” folder INTO c:\inetpub\wwwroot:
</p>

![copy upload file to wwwroot](https://github.com/user-attachments/assets/839f50ed-1b31-4589-a8a5-d2de0dc51c20)

<p>
	Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”:
</p>
<p>
</p>
<br />
<br />

	
 Click “Enable or disable an extension” in IIS PHP Manager
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

  ![enable extension](https://github.com/user-attachments/assets/68c8e865-321e-471e-9a74-7d51c62d1476)

</p>
<br />
<br />
<br />
<p>
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
  
![rename to ostconfig](https://github.com/user-attachments/assets/8be21820-98d9-4986-b28a-96e1ce768002)

</p>
<br />
<br />
<h3 align="center">Assign Permissions: ost-config.php</h3>
<br />
<p>
	Disable inheritance -> Remove All:

  New Permissions -> Everyone -> All:
</p>
<p>
	
  ![assign permissons](https://github.com/user-attachments/assets/ddf566cd-dfa0-4214-ac66-3b6494b92e77)

</p>
<p>
</p>
<br />
<br />
<br />
<p>
</p>
<h3 align="center">Download and Install HeidiSQL</h3>
<br />
<p>

![install heidisql](https://github.com/user-attachments/assets/2d23f8d0-c584-491a-9b71-13c3d14667de)

</p>
<p>
	Create a new session, root/root
</p>
<p>
	Connect to the session:
</p>
<p>
</p>
<p>
	Create a database called “osTicket”:
</p>
<p>
	
![setup mysql](https://github.com/user-attachments/assets/42b4a93e-a068-4540-9aa9-7e2c0362cb58)

</p>
<br />
<br />
<h3 align="center">Continue Setting up osTicket in the browser</h3>
<br />
<p>MySQL Database: osTicket</p>
<p>
</p>
<p>
</p>
<p>
	
</p>
<p>Click “Install Now!”</p>
<p>Congratulations, Hopefully Its Installed With No Errors
<p>
</p>

![done](https://github.com/user-attachments/assets/aab6b332-4ec7-4f32-b3a9-3c1deefe983d)

<br />
<p>
<h3 align="center">Login to the osTicket Admin Panel (http://localhost/osTicket/scp/login.php)</h3>
<br />
<p>
</p>
<h3 align="center"> Congrats, You've Finished Installing osTicket.</h3>
