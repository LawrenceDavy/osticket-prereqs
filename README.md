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

- Azure Virtual Machine
- Internet Information Services (IIS)
- PHP Manager
- Rewrite Module
- VC Redist
- MySQL
- Heidi SQL
- osTicket v1.15.8
- Link to downloads: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6

<h2>Installation Steps</h2>

<br>

![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/432fc1e6-a32b-4a43-9e00-7e0a29631067)
![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/73947bf3-7a62-46ed-82c8-dd646c82d462)
- First we need to create a resource group and virtual machine(VM) to host our osTicket software. A Virtual Network (Vnet) will be auto-created while the VM is being made.
- Remember to save/write down the username and password you need to enter during setup. We will need these credentials to log into our Windows 10 machine.
- Since osTicket does not require alot of resources in order for it to run effectively we will be using a standard ssd drive with 2 virtual cpu's and 8GB of ram.
- The operating system of choice was Windows 10.

<br>
<br>

![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/84c19029-d978-426f-ac33-c61fdb401fa0)
- Login into the server using Windows Remote Desktop using the public IPv4 that was given when the virtual machine was created.
- Enter the credentials you chose when setting up the VM.

<br>
<br>

![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/6bac743e-9699-4135-8a45-1c2cd92bc5ba)
<br>
Once logged in, navigate to Windows Features to install IIS, CGI and HTTPS Features:
Windows Key --> type Windows Features --> select the first entry Turn Windows Features On or Off.
CGI and Common HTTP Features
 - World Wide Web Services -> Application Development Features ->
  - [X] CGI
  - [X] Common HTTP Features
IIS Management Console
  - Internet Information Services -> Web Management Tools -> IIS Management Console
   - [X] IIS Management Console

<br>
<br>

![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/fc33b8d1-c30c-4bde-851a-55ab886976e9)
![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/4a54be5c-4d86-474a-8041-ffffdaf4f97c)
<br>
Install PHP Manager for IIS and Rewrite Module.
<br>
https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view?usp=drive_link
https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view?usp=drive_link

<br>
<br>

![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/a3c468e4-f691-4a93-8d08-ec3997bfd04d)
![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/50d3fe60-948d-42fc-bfe2-1d799de739b8)
<br>
Download the PHP zip file.
<br>
https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view?usp=drive_link
<br>
Create the directory C:\PHP. This is were we will extract our PHP download into.

<br>
<br>

![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/4a320f84-8ae8-49c2-abe9-2c4dd3300e6c)
<br>
Install Microsoft VC Redist(x86)
<br>
https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view?usp=drive_link

<br>
<br>

![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/6a18a747-36c6-41a1-9bdd-7e546865b5ad)
![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/c8e94a5b-6d18-4a18-8da1-adb87bf467b7)
<br>
Install mySQL server with typical setup.
Launch Configuration Wizard after install and use standard configuration.
When prompted, enter a password that you can remember.

<br>
<br>

![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/44887438-ed85-4572-8fbf-dd6bfb852fcc)
Open IIS as an administrator.
Register PHP from within IIS.
Reload IIS (Open IIS, Stop and Start the server)

<br>
<br>

![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/7c18fba0-ad72-431e-8fd1-8edefa649bb9)
<br>
Download osTicket
https://drive.google.com/file/d/1VeVXKlzHDRjeaVUL99ptq7qYbrbXdFxJ/view?usp=drive_link
<br>
Extract and copy “upload” folder to c:\inetpub\wwwroot
Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”
Reload IIS (Open IIS, Stop and Start the server)


![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/feec24bb-45b7-4cd5-9b5d-cc1fd007c935)

![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/bd38aef3-b0ba-4169-8542-f6838ca56499)

![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/5565df9c-65c6-46cc-aea9-1b4a3ea05009)

![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/6110a91e-c596-4a4c-bdce-fe5390bc17dc)

![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/8a9016c5-8c80-4faa-af51-20087a658f7b)

![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/13829d01-b41b-4c0d-b650-4646bac26344)

![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/21ac844b-7ea8-4c94-a2d7-202a68068a3f)

![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/9f359ab9-6a01-4dd1-9709-6d490d45f8eb)

![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/84735928-e4ee-4445-aaaf-58bb21cabc1c)

![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/d49bfbf4-239c-4191-b4a9-2f1b6031ac47)

![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/a1763e07-8296-4cb8-9221-b2791f79229c)

![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/cef1a172-a88e-406e-a4ff-57f648d814d7)

![image](https://github.com/LawrenceDavy/osticket-prereqs/assets/24421979/4cc67f2b-c01c-440f-8f64-4bf15a20c5ab)
