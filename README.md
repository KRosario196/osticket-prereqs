<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Microsoft Remote Desktop (RDP)
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> 

<h2>List of Prerequisites</h2>

- Azure Virtual Machine
- osTicket Installation files
- Heidi SQL

<h2>Installation Steps</h2>

<p>
</p>
<p>
Welcome to my comprehensive IT tutorial! To get started, we'll set up a Virtual Machine (VM) using the Microsoft Azure portal (portal.azure.com). A VM acts as a remote computer, allowing us to safeguard our physical machine in case of any issues, while also providing a fresh environment for ongoing lab experiments. First, create a resource group and name it "osTicket." Then, proceed to create a VM with 2 to 4 CPUs; in this instance, I’ll be opting for 4 CPUs.
  
 <img src="https://i.imgur.com/OPaIGoN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<p>
</p>
<p>Next, connect to your newly created VM using RDP with the public IPv4 address. If you’re on a Mac, you’ll need to download Microsoft Remote Desktop (RDP). 
</p>
<img src="https://i.imgur.com/uLVKzxS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
</p>
<p>
Now that you’re connected to your VM, it’s time to enable IIS. Start by opening the Control Panel and selecting "Uninstall a program." Then, look to the left and click on "Turn Windows features on or off." A list will appear, where you can enable Internet Information Services.
</p>  
<img src="https://i.imgur.com/qtEnuWu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
</p>
<p>
Great! Now that IIS is enabled, we need to install the Web Platform Installer. You can find everything you need to download for setting up osTicket at this link: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6. Just click the link and install the Web Platform Installer.
</p>
<img src="https://i.imgur.com/AxHCfQ6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>  
</p>
<p>
After you’ve installed the Web Platform Installer, launch the application. Within it, you’ll need to install MySQL 5.5, followed by the x86 version of PHP, up to 7.3. You may encounter some failed installations, such as the C++ redistributable package, PHP 7.3.8, and PHP Manager for IIS. These files can be found through the installation link provided.
</p>
<img src="https://i.imgur.com/JJ8bZeJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
</p>
<p>
Next, download osTicket and then extract the files. Copy the "upload" folder into c:\inetpub\wwwroot, and afterwards, rename the folder to osTicket.
</P>
<img src="https://i.imgur.com/TUGiSKi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<p>
</p>
<p>
Open IIS Manager and restart the server. In IIS Manager, navigate to Sites -> Default -> osTicket. On the right side, click "Browse *:80." This will open your default browser and display the osTicket web server.
</p>
<img src="https://i.imgur.com/4AkTkV0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p>
</p>
<p>
Return to IIS Manager and enable some extensions. Navigate to Sites -> Default -> osTicket, then double-click on PHP Manager. Click on "Disable or enable an extension," and enable both "php_intl.dll" and "php_opcache.dll." After that, refresh the osTicket web server to see the changes; the "Intl Extension" should now be enabled. 
</p>
<img src="https://i.imgur.com/APZgUTT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p>
</p>
<p>
Go back into c:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php rename the file to c:\inetpub\wwwroot\osTicket\include\ost-config.php
Assign permissions to ost-config.php Disable inheritance->Removeall
New Permissions->Everyone->all
</p>
<img src="https://i.imgur.com/1nYaYGe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p>
</p>
<p>
Next, proceed with the osTicket setup in your browser by clicking "Continue." Here, you can name the Helpdesk as you wish and select a default email address that will receive messages from customers who submit tickets. 
</p>
<img src="https://i.imgur.com/RmVk3q5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<p>
<p>Continue Setting up osticket in the browser MySQL Database: osTicket MySQL Username: root MySQL Password: Password1 Click “Install Now!”
Congratulations, hopefully it is installed with no errors!
Clean up
Delete: C:\inetpub\wwwroot\osTicket\setup
Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php
Login to the osTicket Admin Panel (http://localhost/osTicket/scp/login.php)
