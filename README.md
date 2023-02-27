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

- Created a resource group on Azure
- Created a Windows virtual machine
- Logged into virtual machine with remote desktop
- Item 4
- Item 5

<h2>Installation Steps</h2>

<p>
Enable IIS in Windows with CGI

- Right click on the Windows icon on the bottom-left of the toolbar
- Go to "Control Panel" -> "Programs"
- Click on "Turn Windows Features on or Off"
- Check on the box to the left of "Internet Information Services"
- Expand "Internet Information Services", "World Wide Web Services", and "Application Development Features"
- Check "CGI"
- Click "OK"
  
</p>
<p>
<img src="https://i.imgur.com/Mizd40v.png" height="80%" width="80%" alt="IIS Setup"/>
</p>

<hr>

<p>
Prerequisite Installation Files
  
- Open this [link](https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6) on a browser like Edge to access files/downloads to be able to set up osTicket
  
</p>

<hr>

<p>
Install PHP Manager and Rewrite Module
  
- Download and install the "PHP Manager" - PHPMangerForLLS_V1.5.0msl, from the installation files
- When installing, just keep clicking "Next" and "I agree"  
- Download and install the "Rewrite Module" - rewrite_amd64_en-US.msl 
  
</p>

<hr>

<p>
Create PHP Manager
  
- Open the "File Explorer" on your toolbar
- Go to "This PC" -> "C:"
- Create a new folder named "PHP" by right-clicking a whitespace in the folder
  
</p>
<p>
<img src="https://i.imgur.com/pEwxvQm.png" height="80%" width="80%" alt="php folder"/>
</p>

<hr>

<p>
Install PHP
  
- Download and install "PHP7.3.8" from the installation files
- Right click the downloaded folder in your file explorer to extract all
- Select "C:\PHP" as the file destination then "Extract"

</p>

<hr>

<p>
Install VC_redist and MySQL
  
- Download and install "VC_redist.x86.exe" just like any other installation
- Download and install "mysql-5.5.62-win32.msl"
- During the installation of MySQL, modify the security settings to be able to create your own password.
  
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

