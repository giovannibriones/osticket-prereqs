![1](https://github.com/giovannibriones/osticket-prereqs/assets/163789590/e33517d9-2225-44a4-957e-003ecbb363de)

</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 (22H2)</b> 

<h2>List of Prerequisites</h2>

- IIS
- PHP Manager
- VC_redistx86
- MySQL 5.5.62
- Rewrite Module
- Heidi SQL

<h2>Installation Steps</h2>

<p>
</p>
<p>
<h3>&#9312; Create a Virtual Machine on Azure</h3>
The first step to do is to create a virtual machine on Azure. 
Choose the image or base operating system as Windows 10 Pro, version 22H2.</p>
<p>

<img width="758" alt="2" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/23d9667e-c26e-4f88-9285-d448c63026f9">

<p>
</p>
<p>
<strong> NOTE: Make sure to set the size to at least 2 vcpus and 16 GiB memory. 
And make sure that RDP (3389) is allowed in "Select inbound ports" in order to permit Remote Desktop access to the VM.</strong> </p>
<p>

<img width="757" alt="3" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/82b2c67a-3b78-43c8-8980-8725923375ad">



</p>
<br />

<p>
</p>
<p>
<h3>&#9313; Review and Create </h3>
<p>Click on the last check box to make sure an eligible Windows 10 license is had. Then continue to "Review + create". A validation process will happen. Then once the validation is successfully accomplished and is a pass, proceed to create.</p>

</p>
<br>
<h3>&#9314; Find your VM's public IP address</h3>
<p></p>Permit some time for the deployment to complete then find the VM's public IP address and copy it.</p>
<p>
<img width="1009" alt="4" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/941a738c-e208-4aac-a182-acfcec531367">



</p>
<p>
<h3>&#9315; Connect to the VM using the Remote Desktop Connection program</h3>
<p>Open your Remote Desktop Connection program and paste the VM's IP and login with the same login credentials used to create the VM.</p>
<p>
<img width="302" alt="5" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/f285eec1-0d5c-4246-bd4f-04fb508f534e">



</p>
<br />
<h3>&#9316; Enable IIS </h3>
<p> Once the VM is open, the next step is to install / enable IIS. For that, the Control Panel needs to be accessed and the programs applet opened. Under programs, "Turn Windows features on or off" needs to be selected.</p>
<p> <img width="552" alt="6" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/adbf4223-9ff9-4101-a589-4ef0d8e7796b">


  
</p>
<p>Then, enable and expand the following features:</p>
<p><img width="295" alt="7" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/26ceaf15-fffc-4fc9-a36c-cf93a237a6b0">

</p>

<p> [X] Internet Information Services</p>
<p>[X] Web Management Tools </p>
<p>[X] IIS Management Console </p>
<p>[X] World Wide Web Services  </p>
<p>[X] Application Development Features </p>
<p>[X] CGI</p>
<p>[X] Common HTTP Features</p>
<br>
<p> Click okay and the features should be enabled.</p>
<br>
<p> <strong> NOTE: To quickly verify whether the changes were successfully configured, simply type 127.0.0.1 on a browser and the page below should appear. </strong></p>
<img width="1094" alt="8" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/31cc67ff-0588-4591-b084-16bf4dd457d1">

<br> <br>
<h3>&#9317; Download and Install PHP Manager</h3>
<p> To download and install PHP manager, you can by accessing the <a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> installation files </a>(PHPManagerForIIS_V1.5.0.msi) 
</p> <br>
<p><img width="386" alt="9" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/62dddfb0-16f0-41ed-86f9-3995eb06dd7d">

</p> 
<br>
<h3>&#9318; Download and Install the Rewrite Module</h3>
<p>To download and install the rewrite module (rewrite_amd64_en-US.msi), you can by accessing the <a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> installation files </a> </p>
<p><img width="647 "alt="9" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/8bbf00f0-f41b-4c51-b90a-84f0f2a98f86">

</p>
<h3>&#9319; Create a new directory</h3>
<p>Continue to File Explorer and create the directory C:\PHP </p>
<img width="647" alt="11" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/01c2ae2e-446c-4292-9a99-ee652daee47a">

<br>
<br>
<h3>&#9320; Download and install php-7.3.8-nts-Win32-VC15-x86.zip </h3>
<p> Download and install php-7.3.8-nts-Win32-VC15-x86.zip, you can be accessing the <a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> installation files </a> and unzipping the contents into the newly created folder located at C:\PHP </p>
<img width="631" alt="12" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/6ad92189-30c6-48ee-a0c0-c4a884130c7f">

<br>
<h3>&#9321; Download and install VC_redist.x86.exe </h3>
<br>
<h3>&#9322; Download and install MySQL 5.5.62 </h3>
<p> To download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi), you can by accessing the <a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> installation files </a>  and configure in accordance to the following; </p>
<p> [X] Typical Setup</p>
<p>[X] Launch Configuration Wizard after install </p>
<p>[X]Standard Configuration 
</p>
<br>
<img width="383" alt="13" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/d4eb4f5f-a923-4683-9bf8-cb96869b70b6">

<br>
<h3>&#9323; Launch IIS as an administrator</h3>
<p> Search for IIS in the Windows search bar and right click it and choose open as Administrator</p>
<br>
<h3>&#9324; Register PHP Manager </h3>
<br>
<img width="682" alt="14" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/ada44197-55a4-4c96-beba-703156fca967">


<br>
<br>
<p><strong> NOTE: Registration will require you to provide a path to "php-cgie.exe". Direct it to the PHP folder created before and you will locate the file that is being asked for. 
</strong></p>
<br>
<img width="623" alt="15" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/7dd8ba1b-6709-4b18-8350-b1db5d987228">

<br>
<p>
</p> 
<h3>&#9325; Restart the IIS server</h3>
<p> The restart button can be found on the right side of the window.</p>
<br>
<img width="623" alt="16" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/11bc6c19-711d-4414-9088-f20551772504">

<br>
<br>
<h3>&#9326; Download and install osTicket</h3>
<p> Download and install osTicket v1.15.8 from the installation files and extract the contents to c:\inetpub\wwwroot </p>
<br>
<img width="547" alt="17" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/ce997e99-d53d-4e47-b652-4dccffe7ba93">

<p> Inside c:\inetpub\wwwroot, Rename “upload” to “osTicket”</p>
<br>
<br>
<h3>&#9327; Restart the IIS server again.</h3>
<img width="623" alt="18" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/5910d134-5bcd-4c12-8b39-02371e6440b4">

<br>
<br>
<h3>&#9328; Launch osTicket </h3>
<p>On the left hand side of IIS, Expand on the VM name -> Sites - > Default Website -> osTicket </p>
<img width="623" alt="19" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/892d71d4-7344-41f9-8c32-3beb4dcb31a9">

<p></p>
<p><strong>NOTE: Make sure to click on osTicket</strong></p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<h3>&#9329; Click on Browse *80 to launch osTicket</h3>
<p> On the right side of the window, click on browse *80 </p>
<img width="623" alt="20" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/717578c3-c2d8-4c69-bbf1-01ef8de9a606">

<br>
<br>
<br>
<p><strong>This should the cause the browser to open osTicket</strong>.</p>
<br>
<br>
<img width="664" alt="21" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/0223308b-1b1e-49b4-b480-64e5c5508e9e">

<br>
<br>
<br>
<h3>&#9330; Enable extensions</h3>
<p>Open IIS and click on PHP Manager and select "enable or disable extension". </p>
<p>Enable the following extensions:</p>
<p>[X]Enable: php_imap.dll</p>
<p>[X]Enable: php_intl.dll</p>
<p>[X]Enable: php_opcache.dll</p>
<img width="273" alt="22" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/46300aec-3d0c-480c-85ed-d76850928824">

<br>
<br>
<br>
<h3>&#9331; Refresh osTicket</h3>

<p>Refresh the osTicket page on the browser and notice some extensions will now appear active.</p>
<img width="608" alt="23" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/8987ca1e-de41-46ef-9a5f-45cef20fead4">

<br>
<br>
<br>

<h3>&#12881; Rename ost-config.ph</h3>

<p> Under C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php, rename "ost-sampleconfig.ph" to "ost-config.ph"</p>
<img width="527" alt="24" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/dbbd4551-331c-4ed5-bce1-abf405a9381b">

<br>
<br>
<br>

<h3>&#12882; Configure ost-config.ph permissions</h3>

<p>Configure ost-config.php permissions by right-clicking and choosing</p>
<p>Properties -> Security -> Advance -> Disable inheritance</p> 
<p>Choose remove all inherited permissions and add everyone as a principal. Choose all boxes to make sure all permissions are given. </p>
<img width="571" alt="25" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/9d82210c-f2c6-4666-81bd-eca5c636a6b2">

<p><strong>.</strong></p>
<p><strong>.</strong></p>

<h3>&#12883; Proceed with the osTicket installation</h3>

<p> Proceed with the osTicket installer on your browser by completing the first half of the page.</p>
<img width="611" alt="26" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/a6745182-4138-4529-88ec-ffdf279dd78c">

<br>
<br>
<p><strong>NOTE: Concern should not be had about the database credentials. Those will be filled at a later time.</strong> </p>
<br>
<p><strong>.</strong></p>
<p><strong>.</strong></p>

<h3>&#12884; Download and install Heidi SQL from the installation files</h3>

<p>Open Heidi SQL and create a new session. Be certain to fill in the username as root and create a password. After inputting credentials, click open and a new session should appear.
</p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>

<h3>&#12885; Create new database </h3>

<p>On the left side of the window, right click on "Unnamed" and click create new database and name it "osTicket".</p>
<img width="512" alt="27" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/33b7f850-73a3-489a-8ccf-60f50d6fe94b">

<br>
<br>
<p><strong>.</strong></p>
<p><strong>.</strong></p>

<h3>&#12886; Complete the signing up process</h3>

<p>Return to the osTicket browser and complete the missing credentials. 
It should look something like this.</p>
<img width="308" alt="28" src="https://github.com/giovannibriones/osticket-prereqs/assets/163789590/13d08112-2396-4c73-9a1e-c8300a1d160c">


<p><strong>.</strong></p>
<p><strong>.</strong></p>

<h3>&#12887; Complete the osTicket installation</h3>

<p>Click install and osTicket should begin setting up. </p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>

<h2> Final cleanup steps</h2>
<p>[X] Delete "setup" file located at C:\inetpub\wwwroot\osTicket\setup</p>
<p>[X] Set permissions of "ost-config.php" to read only.</p>
<p> File is located at C:\inetpub\wwwroot\osTicket\include\ost-config.php</p>
<br>
<br>
<h1>Felicitations! &#127881; osTicket has been successfully installed!</h1>
