# Prerequisites-for-OSTicket

![image](https://github.com/user-attachments/assets/6469e8b7-253d-45f0-8bc6-d5d272c79e08)

# How to Install osTicket

This is an easy guide to installing a help desk ticketing system called osTicket.
Files You Need to Download

# Required Downloads
### [Download Here](https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6) 📁

# Software & Technologies Used

Windows 10 (Build 19044)

Microsoft Azure (Virtual Machines)

Remote Desktop (RDP)

Internet Information Services (IIS)

# Prerequisites

Create a Virtual Machine in Azure

Install osTicket v1.15.8

Install HeidiSQL

Install MySQL

Install PHP

install Microsoft Visual C++ Redistributable

# Steps

Create Virtual Machine in Azure


First, start by creating a Resource Group inside Azure.

![image](https://github.com/user-attachments/assets/83df0135-e585-447e-8c26-f4e14b32bcfd)

Now, create a Windows 10 Virtual Machine (VM), typically with 2-4 Virtual CPUs. For username and password, it can be anything as we'll be using this info to remote in with our main computer. When creating the Virtual Machine (VM), allow Azure to create a new Virtual Network (Vnet):


![image](https://github.com/user-attachments/assets/741b057b-c58f-482e-aff7-c6ec7e76cc86)


Open your Remote Desktop Connection app on your computer and connect to your Virtual Machine that was created in Azure.


![image](https://github.com/user-attachments/assets/4ca2fbf5-7a1f-4493-9228-8043c7bd17be)


Now we need to install / Enable IIS in Windows. Go to your Search Bar > Type "Control Panel" > Click "Programs" > "Turn Windows features on or off" > Scroll down to "Internet Information Services (IIS).


![image](https://github.com/user-attachments/assets/104d5800-d7e8-4653-8c9e-b4aa57008cd0)


Once clicked, find the "Internet Information Services" expand it and then expand the "World Wide Web" tab. Afterward, expand the application Developer tab. Finally check the "CGI" button & press Ok. You will need CGI to download the PHP Manager. The PHP manager is a back-end web programming language that allows osTicket to run off a web browser.


![image](https://github.com/user-attachments/assets/7f9e6db7-46cc-48fb-8488-d59c12f4fef5)


# Install PHP Manager


Download the PHP manager file, and agree with all the terms. We've now downloaded the PHP manager into our operating system.


![image](https://github.com/user-attachments/assets/638bc7f6-e478-4e70-8612-614d0e12b332)


# Install Rewrite Module


Download the Rewrite Module file, agree with all the terms and it should now be installed onto the Computer.


![image](https://github.com/user-attachments/assets/32d67220-1e1b-405c-9d3c-632fbbd41b99)


# CREATE DIRECTORY C:\PHP


Open File Explorer, type, "C:\" in the search bar, Right-click and create a new folder called, "PHP". Download php-7.3.8-nts-Win32-VC15-x86.zip from Files You Need to Download, Extract it by going to where you download the file, Right-click the PHP 7.3.8 file and press extract to the PHP Folder you just created.


![image](https://github.com/user-attachments/assets/e7e06e8a-2c66-47a7-a887-37592c7439b6)


VC_REDIST DOWNLOAD

Download and install VC_Redist, Agree with any terms and agreements and finish installing.


![image](https://github.com/user-attachments/assets/ab74dac6-042b-46ad-9230-cdcae8910dab)


DOWNLOAD MySQL

Download and install MySQL, Agree with any terms and agreements up until you get to the password portion. Here you can create a username and password for the database that you'll be using to store the Ticket Information used in osTicket.


![image](https://github.com/user-attachments/assets/e2e4d2e1-2781-43bb-827e-81e4b4138fb6)

![image](https://github.com/user-attachments/assets/5d4a9277-4241-4e7c-9d3c-a5da80ad6277)


# Install osTicket v1.15.8


Download osTicket (download from within lab files: link).

Extract and copy the “upload” folder INTO c:\inetpub\wwwroot:


![image](https://github.com/user-attachments/assets/adf95fe7-3174-4721-811b-fc3eff0c8864)

![image](https://github.com/user-attachments/assets/9abc1965-77ee-40e2-b55c-42d454d4d404)

Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”:

![image](https://github.com/user-attachments/assets/2b418e3e-8987-4efb-ab2e-972e16703b96)


# Reload IIS (Open IIS, Stop and Start the server)


Go to sites -> Default -> osTicket:




![image](https://github.com/user-attachments/assets/5b69fe06-d155-4e75-8840-6882eb3e178d)

On the right, click “Browse *:80”:

![image](https://github.com/user-attachments/assets/9748ac48-39bd-4f76-95ee-65a00c461273)

Enable Extensions in IIS: Note that some extensions are not enabled


Go back to IIS, sites -> Default -> osTicket.

Double-click PHP Manager:


![image](https://github.com/user-attachments/assets/a3a887cd-d9f4-4571-a1d1-123ec6b88159)

Click “Enable or disable an extension”.

Enable: php_imap.dll.

Enable: php_intl.dll.

Enable: php_opcache.dll:




