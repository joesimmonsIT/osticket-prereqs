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

- Resource Group
- Virtual Machine
- Remote Desktop
- Enable ISS
- Test Web Services
- PHP Manager Install
- Rewrite Module
- PHP Directory
- PHP Download
- PHP Extraction
- VC Redistribution Download
- MySQL Server Installation
- PHP Registration with IIS
- OsTicket Installation
- Heide SQL Installation
- OsTicket Confirmation
  

<h2> Resource Group</h2>

<p>
<img src="https://i.imgur.com/SIGcx5L.png"/>
</p>
<p>
Go to Azure Portal: Portal.Azure.com
</p>
<br />

<p>
<img src="https://i.imgur.com/3AkpqDH.png"/>
</p>
<p>
Go to the search bar and type "resource group". <br /> <br />
Select "Resource Groups" from the search results. <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/D78ERNh.png"/>
</p>
<p>
Select "Create" in the middle of the page.
</p>
<br />

<p>
<img src="https://i.imgur.com/VSA6Bjl.png"/>
</p>
<p>
Subscription: Select the desired subscription, if you have more than one Azure subscription. <br /> <br />
If you only have one subscription skip this step and move on to the next step. <br /> <br />
Resource group: Select the desired name of the resource group, for this tutortial we will be using "RGosTicket". <br /> <br />
Region: Select the desired Region, for this tutortial we will be using (US) East US. <br /> <br />
Select "Review + create" to proceed with creating the resource group. <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/D2Jq2sM.png"/>
</p>
<p>
Once everything is completed correctly you will see a green check mark and the words "Validation passed". <br /> <br />
Select "Create" to proceed with the creation of the resource group. <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/WWCBzRP.png"/>
</p>
<p>
The creation of the Resource Group "RGosTicket" has been completed and new additional resources can be created <br />
and added to the resource group.
</p>
<br />

<h2> Virtual Machine </h2>
<p>
<img src="https://i.imgur.com/ed6AeZG.png"/>
</p>
<p>
Go to the search bar and type "virtual machines". <br /> <br />
Select "Virtual machines" from the search results. <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/RsMGB9Y.png"/>
</p>
<p>
Select "+ Create". <br /> <br />
Select "Azure virtual machine". <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/0LTaNMJ.png"/>
</p>
<p>
Subscription: Select desired subscription if you have more than one Azure subscription. <br /> <br />
If you only have one subscription skip this step and move on to the next step. <br /> <br />
Resource group: Select desired resource group, for this tutorial we will be using "RGosTicket". <br /> <br />
Virtual machine name: Select desired virtual machine name, for this tutorial we will be using "VM-osticket". <br /> <br />
Region: Select desired region, for this tutortial we will be using "(US) East US". <br /> <br />
Availability Zone: Select the desired zone, for this tutorial we will be using "Zone 2". <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/oP3BC2n.png"/>
</p>
<p>
Image: Select "Windows 10 Pro".
</p>
<br />

<p>
<img src="https://i.imgur.com/9vZQZr8.png"/>
</p>
<p>
Size: Select "Standard - 2 vcpus". <br /> <br />
Username: Select desired username, for this tutorial we will be using "labuser". <br /> <br />
Password: create a password you can easily remember or one you can document and retreive easily. <br /> <br />
Confirm Password: Repeat the same password you recently created. <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/lRRIR7d.png"/>
</p>
<p>
Acknowledge the Licensing Confirmation, a blue box with a white check mark should appear. <br /> <br />
Select "Review + create" to proceed with creating the virtual machine. <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/vwejzzI.png"/>
</p>
<p>
Once everything is completed correctly you will see a green check mark and the words "Validation passed". <br /> <br />
Select "Create" to proceed with the creation of the virtual machine. <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/jN36w5t.png"/>
</p>
<p>
The deployment (creation) of the virtual machine is in progress.
</p>
<br />

<p>
<img src="https://i.imgur.com/jxdhXNi.png"/>
</p>
<p>
The deployment (creation) of the virtual machine is completed.
</p>
<br />

<h2> Remote Desktop </h2>
<p>
<img src="https://i.imgur.com/wjZwQyw.png"/>
</p>
<p>
Go to the Portal: Portal.Azure.com. <br /> <br />
Type "Virtual Machines" in the search box. <br /> <br />
Select "Virtual machines" from the search results. <br /> <br />
Select "VM-osticket". <br /> <br />
Copy Public IP Address. <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/dp3CNIS.png"/>
</p>
<p>
Paste Public IP Address. <br /> <br />
Press Connect. <br /> <br />
</p>
<br />

<h2> Enable ISS </h2>
<p>
<img src="https://i.imgur.com/Ysb3xlc.png"/>
</p>
<p>
Once connected to Remote Desktop Connection, go to the Windows Pane. <br /> <br />
In the search bar type "run" and Press Enter. <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/Pw3eT5o.png"/>
</p>
<p>
Type "Control Panel" and Press "Ok".
</p>
<br />

<p>
<img src="https://i.imgur.com/U54ztFS.png"/>
</p>
<p>
Select "Programs".
</p>
<br />

<p>
<img src="https://i.imgur.com/d8Ac0Ad.png"/>
</p>
<p>
Select "Turn Windows features on or off".
</p>
<br />

<p>
<img src="https://i.imgur.com/Vhb87VX.png"/>
</p>
<p>
Check the box for "Internet Information Services".
</p>
<br />

<p>
<img src="https://i.imgur.com/Xkf8b4i.png"/>
</p>
<p>
Collapse Internet Information Services. <br /> <br />
Check box for World Wide Web Services. <br /> <br />
Collapse World Wide Web Services. <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/vvTAejw.png"/>
</p>
<p>
Check box for Application Development Features. <br /> <br />
Check box for "CGI". <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/kfkjiaO.png"/>
</p>
<p>
Collapse Common HTTP Features. <br /> <br />
Make sure all the boxes are checked. <br /> <br />
Select "Ok".
</p>
<br />

<p>
<img src="https://i.imgur.com/LTntcta.png"/>
</p>
<p>
Windows is processing requested changes. <br /> <br />
Press "Close" to exit screen. <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/uWlhAYr.png"/>
</p>
<p>
Open a new browser. <br /> <br />
Type "127.0.0.1". <br /> <br />
</p>
<br />

<h2> Test Web Services </h2>
<p>
<img src="https://i.imgur.com/SckDSBQ.png"/>
</p>
<p>
Press Enter. <br /> <br />
Internet Information Services image will appear this means it is ready for the prerequisites to be installed to be fully functional. <br /> <br />
</p>
<br />

<h2> PHP Manager Install </h2>
<p>
<img src="https://i.imgur.com/uOPX3YU.png"/>
</p>
<p>
Go to the PHP Manager Link. <br /> <br />
Select "Download". <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/tNgKRpO.png"/>
</p>
<p>
Proceed with "Download anyway".
</p>
<br />

<p>
<img src="https://i.imgur.com/1HNYELj.png"/>
</p>
<p>
Select "Open file".
</p>
<br />

<p>
<img src="https://i.imgur.com/4aOGB0a.png"/>
</p>
<p>
Select "Next".
</p>
<br />

<p>
<img src="https://i.imgur.com/wapoTGq.png"/>
</p>
<p>
Select "I Agree". <br /> <br />
Select "Next". <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/6pC8L0s.png"/>
</p>
<p>
PHP Manager installation is complete. <br /> <br />
Select "Close" to exit screen. <br /> <br />
</p>
<br />

<h2> Rewrite Module </h2>
<p>
<img src="https://i.imgur.com/sHtWFmA.png"/>
</p>
<p>
Go to Rewrite Module Link. <br /> <br />
Select "Download". <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/Jof1Tgu.png"/>
</p>
<p>
Select "Download anyway".
</p>
<br />

<p>
<img src="https://i.imgur.com/Svm9b0Z.png"/>
</p>
<p>
Select "Open file" for rewrite.
</p>
<br />

<p>
<img src="https://i.imgur.com/4NG21cE.png"/>
</p>
<p>
Select "I accept the terms in the License Agreement". <br /> <br />
Select "Install". <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/7zRfTQg.png"/>
</p>
<p>
The Rewrite Module installation has been completed. <br /> <br />
Click "Finish" to exit the Setup Wizard. <br /> <br />
</p>
<br />

<h2> PHP Directory </h2>
<p>
<img src="https://i.imgur.com/qFx9AQg.png"/>
</p>
<p>
Go to the Windows Pane. <br /> <br />
Select the "Folder" to open the File Explorer. <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/1m7YiDM.png"/>
</p>
<p>
Select "This PC".
</p>
<br />

<p>
<img src="https://i.imgur.com/yl9gTYH.png"/>
</p>
<p>
Select "Windows (C:)".
</p>
<br />

<p>
<img src="https://i.imgur.com/6gUwRNs.png"/>
</p>
<p>
In the white space of the C: Drive, Right Click, Select "New", Select "Folder".
</p>
<br />

<p>
<img src="https://i.imgur.com/Gk3SbfX.png"/>
</p>
<p>
Rename the folder "PHP".
</p>
<br />

<h2> PHP Download </h2>
<p>
<img src="https://i.imgur.com/9RfxePS.png"/>
</p>
<p>
Select "php-7.3.8." and Click Download.
</p>
<br />

<p>
<img src="https://i.imgur.com/yhHSZZQ.png"/>
</p>
<p>
Go to File Explorer. <br /> <br />
Select "Downloads". <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/uaqmxBM.png"/>
</p>
<p>
Select "php-7.3.8" folder. <br /> <br />
Right Click, and Select "Extract All". <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/Bq2z6fX.png"/>
</p>
<p>
Click "Browse" to select new destination to have the files extracted.
</p>
<br />

<p>
<img src="https://i.imgur.com/4qF9qHK.png"/>
</p>
<p>
Select "This PC" and then select "Windows (C:)".
</p>
<br />

<p>
<img src="https://i.imgur.com/w4L4pJv.png"/>
</p>
<p>
Select "PHP" folder and Press "Select Folder".
</p>
<br />

<p>
<img src="https://i.imgur.com/nbkaKSG.png"/>
</p>
<p>
Select "Extract".
</p>
<br />

<p>
<img src="https://i.imgur.com/HQ4xzSk.png"/>
</p>
<p>
The "Extraction" is complete showcasing all the files that were extracted.
</p>
<br />

<h2> VC Redistribution Download </h2>
<p>
<img src="https://i.imgur.com/u1wgtvS.png"/>
</p>
<p>
Go to the "VC Redistribution" Link. <br /> <br />
Select "Download". <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/LvuZ01M.png"/>
</p>
<p>
Proceed with "Download anyway".
</p>
<br />

<p>
<img src="https://i.imgur.com/dYl4BTW.png"/>
</p>
<p>
Go to "File Explorer". <br /> <br />
Select "Downloads". <br /> <br />
Select "VC_redist.x86". <br /> <br /> 
</p>
<br />

<p>
<img src="https://i.imgur.com/5vwowbW.png"/>
</p>
<p>
Click "I agree to the license terms and conditions". <br /> <br />
Select "Install". <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/hGc3wzn.png"/>
</p>
<p>
Installation is complete. <br /> <br />
Select "Close" to exit screen. <br /> <br />
</p>
<br />

<h2> MySQL Server Installation </h2>

<p>
<img src="https://i.imgur.com/jI1NAu3.png"/>
</p>
<p>
Go to MySQL Server Link. <br /> <br />
Select "Download". <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/AbGjxX8.png"/>
</p>
<p>
Proceed with "Download anyway".
</p>
<br />

<p>
<img src="https://i.imgur.com/00BplFR.png"/>
</p>
<p>
Go to File Explorer. <br /> <br />
Select "Downloads". <br /> <br />
Select "mysql.....". <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/z2zHvBG.png"/>
</p>
<p>
Select "Next".
</p>
<br />

<p>
<img src="https://i.imgur.com/RQrrJsf.png"/>
</p>
<p>
Select "I accept the terms in License Agreement". <br /> <br />
Select "Next". <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/1Jj7hFc.png"/>
</p>
<p>
Select "Typical".
</p>
<br />

<p>
<img src="https://i.imgur.com/0ZtKO0w.png"/>
</p>
<p>
Select "Install".
</p>
<br />

<p>
<img src="https://i.imgur.com/w5WHB0I.png"/>
</p>
<p>
Select "Finish".
</p>
<br />

<p>
<img src="https://i.imgur.com/MPGUEao.png"/>
</p>
<p>
Select "Next".
</p>
<br />

<p>
<img src="https://i.imgur.com/aTS14Dk.png"/>
</p>
<p>
Select "Standard Configuration". <br /> <br />
Select "Next". <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/O8afT31.png"/>
</p>
<p>
Select "Next".
</p>
<br />

<p>
<img src="https://i.imgur.com/QtOqWyo.png"/>
</p>
<p>
Create password. <br /> <br />
Repeat created password. <br /> <br />
Select "Next". <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/dtRjp4G.png"/>
</p>
<p>
Select "Execute".
</p>
<br />

<p>
<img src="https://i.imgur.com/YrP2FC0.png"/>
</p>
<p>
Select "Finish".
</p>
<br />

<h2> PHP Registration with IIS </h2>
<p>
<img src="https://i.imgur.com/yWQ3UBn.png"/>
</p>
<p>
Go to the Windows Pane, in the search bar type "iis". <br /> <br />
Select "Internet Information Services (IIS) Manager". <br /> <br />
Select "Run as administrator". <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/btL6To4.png"/>
</p>
<p>
Select "PHP Manager".
</p>
<br />

<p>
<img src="https://i.imgur.com/1kiLMwR.png"/>
</p>
<p>
Select "Register new PHP version".
</p>
<br />

<p>
<img src="https://i.imgur.com/VVAK0xu.png"/>
</p>
<p>
Select "..." to browse for "php" file extension.
</p>
<br />

<p>
<img src="https://i.imgur.com/jYfBjVF.png"/>
</p>
<p>
Select "php-cgi". <br /> <br />
Select "Open". <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/dBbxjg0.png">
</p>
<p>
Select "Ok".
</p>
<br />

<p>
<img src="https://i.imgur.com/GKo5JVp.png"/>
</p>
<p>
PHP Extension has been registered.
</p>
<br />

<p>
<img src="https://i.imgur.com/a11vCSC.png"/>
</p>
<p>
Select "VM-osticket".
</p>
<br />

<p>
<img src="https://i.imgur.com/R7maRAH.png"/>
</p>
<p>
Go to Actions on the right. <br /> <br />
Under Manage Server select "Restart". <br /> <br />
This will enable the recent PHP Manage updates we just completed. <br /> <br />
</p>
<br />

<h2> OsTicket Installation </h2>
<p>
<img src="https://i.imgur.com/6dHh5sQ.png"/>
</p>
<p>
Select "osTicket" and Click Download.
</p>
<br />

<p>
<img src="https://i.imgur.com/en1wof7.png"/>
</p>
<p>
Select "Download anyway".
</p>
<br />

<p>
<img src="https://i.imgur.com/HG5LHyv.png"/>
</p>
<p>
Go to File Explorer. <br /> <br />
Select "Downloads". <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/T18Koue.png"/>
</p>
<p>
Go to File and select "Open new window".
</p>
<br />

<p>
<img src="https://i.imgur.com/A2X20fB.png"/>
</p>
<p>
Top Window: Select "osTicket" from Downloads Folder. Select "upload". <br /> <br />
Bottom Window: Select This PC, Windows (C:), inetpub, wwwroot. <br /> <br />
Drag "upload" to "root" folder to copy files. <br /> <br />
</p>
<br />

<p>
<img src="https://i.imgur.com/VrG4LIm.png"/>
</p>
<p>
Copy Files Transfer in progress.
</p>
<br />

<p>
<img src="https://i.imgur.com/9YD8WWW.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/z4vWZ5B.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/OovF5DY.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/1bAjdkD.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/6HtAHoC.png">
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/CAI2ef3.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/7uhlyj2.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/FNChXVZ.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/OnqiGef.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/zWz7pyN.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/VqC4rRa.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/LhiPhz4.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/82s0lLl.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/m4flumL.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/YYNOrQk.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/KL416Ry.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/y3xXdlK.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/ffAvHiP.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/jaeuLkh.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/n0aWZKH.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/PGqq7YY.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/d8OE3z9.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/A7UcOp9.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/HXly2wX.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/3pROn85.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/7DCTvKX.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/U4CVIpZ.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<h2> Heide SQL Installation </h2>
<img src="https://i.imgur.com/2N2eVxe.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/8xmuK0j.png"/>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/ygBAJCr.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/Xk6joan.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/JjQOj8f.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/phn96iY.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/NnBL4tN.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/biAviKh.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/WpFWtlL.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/QA1aKub.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/w1o3jqX.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/BuwXwJR.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/IeKcAvZ.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/fY0geBb.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/QUMOJyB.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/gUFcrqj.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/IKIWRld.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/p3NAxPE.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<h2> OsTicket Confirmation </h2>

<img src="https://i.imgur.com/9sJ5Udo.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/3mhnAko.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/O1OxycO.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<img src="https://i.imgur.com/muOxrIQ.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
