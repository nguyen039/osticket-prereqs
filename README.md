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

- Created a resource group on Azure
- Created a Windows virtual machine
- Logged into virtual machine with remote desktop

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

<hr>

<p>
Register PHP

- Search for "IIS" on the Windows toolbar and right click to choose "Run as Administrator".
- Click "PHP Manager" -> "Register new PHP version"
- Go to the file destination by C:\PHP, and select "php-cgi"  
- Open the selected file and click "OK.

</p>

<p>
<img src="https://i.imgur.com/sZhm8xi.png" height="80%" width="80%" alt="register php"/>
</p>

<hr>

<p>
Install ostTicket
  
- Download and install "osTicketv1.15.8"
- Open up the downloaded file and open another file explorer
- On your newly opened file explorer, locate C:\inetpub\wwwroot
- Drag the "upload" folder into wwwroot, and rename the folder from "upload" into "osticket"
  
</p>  

<hr>

<p>
Enable Extensions
  
- Go to the IIS app
- From there, go to "Sites" -> "Default" -> "osTicket" -> "PHP Manager" -> "Enable or Disable an Extension"
- Enable "php_imap.dll", "php_intl.dll", and "php_opcache.dll"
  
</p>  

<hr>

<p>
Open osTicket
  
- On IIS, click "Sites" -> "Default Web Site" -> "osTicket" -> "Browse *:80"
- A web page of osTicket should pop up.
</p>  
<p>
<img src="https://i.imgur.com/XfpExTT.png" height="80%" width="80%" alt="osticket page"/>
</p>

<hr>

<p>
Rename ost-config.php
  
- Go to the file destination: "C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php"
- Right click on the "ost-config.php" file and click on "Property"
- Then go to "Security" -> "Advanced" -> "Disable Inheritance" -> "Remove all Inherited properties from this item"  
- Next, click on "Add" -> "Select a Principle"
- Input "Everyone" onto the textbox and click "Check Names"
- Apply the changes and click "OK"
  
</p>

<hr>

<p>
Install HeidiSQL
  
- Download and install "HeidiSQL"
- Once installed and opened, click on "New"
- Create a username and password
- Connect to a session and create a database named "osTicket"

</p>

<hr>

<p>
osTicket Setup in Browser  
  
- Switch to your browser, fill out all of the required details
- For "MySQL database" set it to osTicket and "mySqL Username" to "root"
- After the setup is done, the osTicket installation should be done.
  
</p>
<p>
<img src="https://i.imgur.com/jFBbyQS.png" height="80%" width="80%" alt="osTicket"/>
</p>
