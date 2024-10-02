<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

# osTicket - Prerequisites and Installation

## Overview
osTicket is an open-source support ticket system that streamlines customer service operations. It allows organizations to manage and respond to inquiries efficiently, providing a centralized platform for tracking and resolving issues. This guide will help you set up osTicket on a Windows environment, ensuring that you have all the necessary prerequisites and installation steps.

## Environments and Technologies Used
- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

## Operating Systems Used
- **Windows 10** (21H2)

## List of Prerequisites
1. **Web Server**: Internet Information Services (IIht  S) installed.
2. **PHP**: Version 7.2 or higher.
3. **Database**: MySQL.
4. **Composer**: Dependency manager for PHP.
5. **SSL Certificate**: Recommended for secure connections.

## Installation Steps

### Step 1: Install IIS
<p>
<img src="path/to/screenshot1.png" height="80%" width="80%" alt="IIS Installation"/>
</p>
1. Open Control Panel.
2. Go to "Programs" > "Turn Windows features on or off".
3. Check "Internet Information Services" and click OK.

### Step 2: Install PHP
<p>
<img src="path/to/screenshot2.png" height="80%" width="80%" alt="PHP Installation"/>
</p>
1. Download PHP from the official site.
2. Extract files to `C:\PHP`.
3. Add `C:\PHP` to the System PATH variable.

### Step 3: Set Up Database
<p>
<img src="path/to/screenshot3.png" height="80%" width="80%" alt="Database Setup"/>
</p>
1. Install MySQL or MariaDB.
2. Create a database for osTicket.
3. Note down database name, username, and password.

### Step 4: Download and Configure osTicket
<p>
<img src="path/to/screenshot4.png" height="80%" width="80%" alt="osTicket Configuration"/>
</p>
1. Download the latest version of osTicket from the official website.
2. Extract files to your web server's root directory (e.g., `C:\inetpub\wwwroot\osticket`).
3. Navigate to `include/ost-config.php` and configure your database settings.

### Step 5: Complete Installation
<p>
<img src="path/to/screenshot5.png" height="80%" width="80%" alt="Complete Installation"/>
</p>
1. Open a web browser and go to `http://localhost/osticket`.
2. Follow the on-screen instructions to complete the installation.
3. Remove the `setup` directory after installation for security.

## Conclusion
Congratulations! You have successfully installed osTicket on your Windows machine. For further customization and usage, refer to the official documentation.
