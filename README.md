# Deploying-Active-Directory

<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Deploying Active Directory</h1>
This tutorial outlines the preperation of on-premises Active Directory within Azure Virtual Machines.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Part 1 Install Active Directory
- Part 2 Create a Domain Admin user within the domain
- Part 3 Join Client-1 to your domain (mydomain.com)

<h2>Install Active Directory</h2>

![image](https://github.com/user-attachments/assets/222c874b-91e7-4ae3-9b96-ae176fdfb1a9)

<p>
Login to DC-1
</p>

![image](https://github.com/user-attachments/assets/ace8cbd7-7e37-41f0-bd15-0caf638279d5)

<p>
Open Server Manager
</p>

![image](https://github.com/user-attachments/assets/a0d747c4-852a-4b11-a1e7-46ebbbef7528)

<p>
Select Add roles and features
</p>

![image](https://github.com/user-attachments/assets/a5f8d9d5-aad1-4704-b07e-d69a9eebdce2)

![image](https://github.com/user-attachments/assets/75513955-eb45-4101-8c7d-770390c1d627)

![image](https://github.com/user-attachments/assets/8e31841b-5980-4302-94ba-f936975af894)

![image](https://github.com/user-attachments/assets/66420aa8-0dbb-46d9-838d-97d1c0f010b0)

<p>
Install Active Directory Domain Services, be sure not to restart
</p>

![image](https://github.com/user-attachments/assets/4a634a7a-ea69-4d0d-9c79-2a3f7330d2a9)

![image](https://github.com/user-attachments/assets/33c3908f-3211-4750-a5ae-734bab35c869)

![image](https://github.com/user-attachments/assets/0e93ee04-8e38-481e-8c78-1496fd60ba8a)

![image](https://github.com/user-attachments/assets/ebc882c3-e74a-4e1e-bfee-1e31b05d11e6)

<p>
Promote this server to a DC: Setup a new forest as mydomain.com 
</p>

![image](https://github.com/user-attachments/assets/635ddb03-98bf-4cd4-9760-fadc54cffe04)

<p>
Restart and then log back into DC-1 as user: mydomain.com\labuser
</p>

<h2>Create a Domain Admin user within the domain</h2>

![image](https://github.com/user-attachments/assets/3cd72611-c3c9-4198-9c2c-9b4c6c56c748)

![image](https://github.com/user-attachments/assets/24987cd7-2a0d-454a-a5e7-48fa58333d48)

![image](https://github.com/user-attachments/assets/aa2cd9ce-35d0-40ec-b709-908960bb6098)

<p>
In Active Directory Users and Computers (ADUC), create an Organizational Unit (OU) called “_EMPLOYEES”
</p>

![image](https://github.com/user-attachments/assets/24987cd7-2a0d-454a-a5e7-48fa58333d48)

![image](https://github.com/user-attachments/assets/07b1d382-30ca-4f23-a646-47cd16fa92d1)

<p>
Create a new OU named “_ADMINS”
</p>

![image](https://github.com/user-attachments/assets/eabd1741-c15a-42d3-b1d7-386c6f7ff9c3)

![image](https://github.com/user-attachments/assets/fa119d36-c65b-43a3-90f2-b2b035ed5eaa)

![image](https://github.com/user-attachments/assets/b69ec729-0267-4e45-b099-17833f448d30)

<p>
Create a new employee named “Jane Doe”
</p>

![image](https://github.com/user-attachments/assets/38d1ab94-fe36-4494-a54f-53192e2370e5)

![image](https://github.com/user-attachments/assets/0b979c64-f839-4064-bece-b831bb610e01)

![image](https://github.com/user-attachments/assets/79736c28-12f3-4f8f-bca2-4ec98d9412e2)

<p>
Add jane_admin to the “Domain Admins” Security Group
</p>

![image](https://github.com/user-attachments/assets/486aadf0-79a3-4747-853d-b9046e598b98)

<p>
Log out / close the connection to DC-1 and log back in as “mydomain.com\jane_admin”
</p>

<h2>Join Client-1 to your domain (mydomain.com)</h2>

![image](https://github.com/user-attachments/assets/cdcd11ad-8832-4f0f-ac90-ed055a66f17c)

![image](https://github.com/user-attachments/assets/b380f5bf-bd77-4e08-a0bf-f2bd08857695)

![image](https://github.com/user-attachments/assets/5ab2eb46-a84d-42b9-9b22-9acf885f500f)

![image](https://github.com/user-attachments/assets/ffee31a6-d495-4a58-adb2-a638f6b389a0)

<p>
Login to Client-1 as the original local admin (labuser) and join it to the domain (computer will restart)
</p>

![image](https://github.com/user-attachments/assets/5ecf3e80-3877-4ef3-83dd-768c58ed5922)

![image](https://github.com/user-attachments/assets/741845c0-49df-4fc2-9f65-bbac0beaf8e7)

![image](https://github.com/user-attachments/assets/ab7ba717-d648-4017-93f2-e21ab0de12d4)

<p>
Login to the Domain Controller and verify Client-1 shows up in ADUC
</p>




<p>
Lorem ipsum dolor sit amet, 
</p>




<p>
Lorem ipsum dolor sit amet, 
</p>




<p>
Lorem ipsum dolor sit amet, 
</p>

















<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, 
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, 
</p>
<br />
