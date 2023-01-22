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

- Create Virtual Machine in Azure
- Create an Azure Virtual Machine Windows 10, 4 vCPUs
- Install / Enable IIS in Windows with CGI
- Download and install PHP Manager for IIS
- Download and install the Rewrite Module
- Create the directory C:\PHP
- Download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP
- Download and install VC_redist.x86.exe
- Download and install MySQL 5.5.62 
- Open IIS as an Admin/Register PHP from within IIS/Reload IIS (Open IIS, Stop and Start the server)


<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/4jK7ZnX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Essentially, I made a resource group and virtual machine in Azure following the first two prerequisites.
The image above is me about to install and enable Windows IIS with CGI.
</p>
<br />

<p>
<img src="https://i.imgur.com/RQN6HTd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here I eventually downloaded PHP Manager and made a new folder designated for PHP on the Windows C: drive. This is just me extracting the PHP zip onto the new folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/6c69Dqs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
This is an installation of MySQL.
 
</p>
<img src="https://i.imgur.com/VjZTO9z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I open and ran IIS as an administrator, clicked on the the VM file on the top left corner and clicked on PHP manager to register the PHP effectively. As soon after, I reloaded the server.

</p>
<img src="https://i.imgur.com/dPHPFrn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I've downloaded osTicket now, the image above is me opening up the osTicket.zip and moving the "upload" folder in it to c:\inetpub\wwwroot. After, I renamed the upload folder to osTicket.
  
</p>
<img src="https://i.imgur.com/Y1AFsqi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
This is me just reloading the server again on IIS as an administrator while in the osTicket folder. Right after, I click Browse *:80 on the right, opening up osTicket on the browser.
  
</p>
<img src="https://i.imgur.com/Err9aFV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
So osTicket is installed, but I'm still missing some features as you can see in the image above.

</p>
<img src="https://i.imgur.com/FMxhtbt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
So I go back to IIS as an admin of course, and I click on the osTicket folder, and in there I go to the PHP manager to enable extensions. The extensions that were enabled are php_imap.dll, php_intl.dll, and php_opcache.dll.

</p>
<img src="https://i.imgur.com/G7vyyRT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I go back to the browser and go back on the osTicket tab and refresh it. The image above shows that there is no longer an X on the PHP IMAP extension.
  
</p>
<img src="https://i.imgur.com/22glHvf.png" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In here I go to c:\inetpub\wwwroot to the osTicket folder. I open the folder to rename the ost-sampleconfig file to ost-config.

</p>
<img src="https://i.imgur.com/AwbVffe.png" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Soon after I right click ost-config, went into properties>security>advance>add>typed "everyone" in the object name to select text box>check names>advance>edit>check off read and read & execute>apply/ok

</p>
<img src="https://i.imgur.com/7A3A1hg.png" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Downloaded Heidi SQL
  
</p>
<img src="https://i.imgur.com/jdxs7SH.png" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Opened HiediSQL, created a new+ session>right clicked on the unnamed tab>created a new database called osTickets>connected to the session using my username and password I had saved in Azure.
 
</p>
<img src="https://i.imgur.com/CJ0BhGp.png" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Went back to my browser to fill up my credentials on osTickets.
  
</p>
<img src="https://i.imgur.com/auRxKMY.png" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Finished filling out my credentials and it looks like osTickets has been installed successfully. :)
  
</p>
<img src="https://i.imgur.com/IsVM8dI.png" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I go back to c:\inetpub\wwwroot where I delete the setup folder. I then go to the ost-config file>right click>properties>security>advance>edit>check off read and read & execute>apply/ok
  
</p>
<img src="https://i.imgur.com/hGjimhM.png" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 Browsed to my help desk login page: http://localhost/osTicket/scp/login.php
  
 </p>
<img src="https://i.imgur.com/3dUuFYY.png" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Logged in successfully ;)
  


 


  



  
  



