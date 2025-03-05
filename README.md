# Prerequisites-for-OSTicket

![image](https://github.com/user-attachments/assets/6469e8b7-253d-45f0-8bc6-d5d272c79e08)

# How to Install osTicket

This is an easy guide to installing a help desk ticketing system called osTicket.
Files You Need to Download

# Required Downloads
### [Download Now](https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6) 📁

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


Install PHP Manager


Download the PHP manager file, and agree with all the terms. We've now downloaded the PHP manager into our operating system.


![image](https://github.com/user-attachments/assets/638bc7f6-e478-4e70-8612-614d0e12b332)



