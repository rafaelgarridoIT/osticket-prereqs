# osticket-prereqs
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://youtu.be/YIe4odQI5Wk?si=tG8oVeSK68Dl9j4F)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- IIS
- PHP Manager
- VC_redistx86
- MySQL 5.5.62
- Rewrite Module
- Heidi SQL

<h2>Installation Steps</h2>
<h2>Setting up osTicket in Azure VM</h2>

1. <strong>Create Virtual Machine in Azure:</strong>
- <strong>Log into Azure Portal</strong>
- <strong>Create a new VM with Windows Server.</strong>

<img width="2048" height="635" alt="azure_portal_osticket_vm_row_highlighted_v2" src="https://github.com/user-attachments/assets/318c88c3-0ade-407f-af3a-d08402ff3c63"/>



<p>



</p>
<p>

</p>
<br />

<p>
<img width="401" height="241" alt="rdp" src="https://github.com/user-attachments/assets/9400c4d2-bc86-40ec-96b7-40d0844e0f20" />

</p>
<p>
 - Use the VM’s public IP address to connect via Remote Desktop Connection (RDP).
</p>
<br />

<p>
<img <img width="449" height="558" alt="login for rdp" src="https://github.com/user-attachments/assets/287916b9-f9c2-4c77-99a6-99e7d912ca61"/>
/>
</p>
<p>
- Log in using the credentials you created during VM setup (Reggie-admin in this example).
</p>
<br />




<strong>2. Download the osTciket-installation-Files.zip</strong>
<p>
  <img <img width="794" height="419" alt="unzip" src="https://github.com/user-attachments/assets/e9ee5a8d-0190-4fad-a7bc-8a8c7429f50b"/>
 />
</p>
<p>
- Inside your VM download the https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD and unzip it onto your desktop. We will use the files to download osTicket.
</p>
<br />


<strong> 3. Enable ISS with CGI </strong>
<p>
  <img <img width="826" height="438" alt="Screenshot 2025-08-29 102918" src="https://github.com/user-attachments/assets/595ea493-840c-4862-93c9-34da303a275c"/>
/>
</p>
<p>
- Go to the Control Panel > Then go to Programs > Programs and Features > Then on the left side of the screen, click "Turn Windows features on or off.
</p>
<br />



- <strong> Enable (internet information services) World Wide Web Services > Application Development Features > enable CGI </strong>
<p>
  <img <img width="417" height="723" alt="Screenshot 2025-08-29 102947" src="https://github.com/user-attachments/assets/fc1d6183-6fe3-4139-840a-a67a1f438e60"/>
 />
</p>
<p>
</p>
<br />


<strong> 4. Download and Install PHP manager from the osTicket-installation-Files </strong>
<p>
  <img <img width="507" height="415" alt="Screenshot 2025-08-29 103007" src="https://github.com/user-attachments/assets/a497235c-5fa6-46b8-b5b3-8f66cb37456a"/>
 />
</p>
<p>
- (PHPManagerForIIS_V1.5.0.msi)
</p>
<br />




<strong> 5. Download and Install the Rewrite Module</strong>
<p>
  <img <img width="501" height="392" alt="Screenshot 2025-08-29 103020" src="https://github.com/user-attachments/assets/580f7d9f-1b49-4689-b53f-9b7d07a8546f"/>
</p>
<p>
- (rewrite_amd64_en-US.msi) from the osTicket-Installation-Files
</p>
<br />





<strong> 6. Create a directory in the C drive. Name the folder PHP. </strong>
<p>
  <img <img width="828" height="445" alt="Screenshot 2025-08-29 103032" src="https://github.com/user-attachments/assets/ae7026c9-63fe-42e0-b6a5-c181c1334c59"/>

</p>
<p>
- Go to file explorer and create the directory C:\PHP
</p>
<br />



<strong> 7. From the osTicket-Installation-Files install (php-7.3.8-nts-Win32-VC15-x86.zip) into C:\PHP </strong>
<p>
  <img <img width="621" height="469" alt="Screenshot 2025-08-29 103042" src="https://github.com/user-attachments/assets/e0b1976f-54db-4eef-936d-7b78373db59e"/>
</p>
<p>
</p>
<br />




<strong> 8. Download and Install the (VC_redist.x86.exe) </strong>
- Install from the osTicket-Installation-Files
<p>
  <img <img width="481" height="300" alt="Screenshot 2025-08-29 103051" src="https://github.com/user-attachments/assets/f466cf70-2658-49e4-b84b-3487703079af"/>
</p>
<p>
</p>
<br />


<strong> 9. Download and Install MySQL 5.5.62 (mysql-5.5.62-win32.msi)</strong>
- Install from the osTicket-Installation-Files
- Select the following configurations:
     - Typical setup
     - launch configuration
     - Standard configuration
<p>
  <img <img width="500" height="393" alt="Screenshot 2025-08-29 103101" src="https://github.com/user-attachments/assets/2d8746e6-8d6a-4e79-b339-ebe4b7611b70" />
</p>
<p>
</p>
<br />

- <strong>  The user for this service is going to type (root) as the username and the password.</strong>

<p>
  <img <img width="833" height="631" alt="Screenshot 2025-08-29 103113" src="https://github.com/user-attachments/assets/fe8e18d5-c6c7-40ad-8feb-6021038d0efd"/>
</p>
<p>
</p>
<br />


<strong> 10. Launch IIS as administrator </strong>
- Search for IIS in the windows search bar and right click it and select open as administrator
<p>
  <img <img width="824" height="476" alt="Screenshot 2025-08-29 103127" src="https://github.com/user-attachments/assets/1464561d-ea4a-4be8-8cc3-1942b9cd6db0"/>
</p>
<p>
</p>
<br />


<strong> 11. Register PHP from within IIS </strong>
- Open the PHP manager
- Register new PHP version
<p>
  <img <img width="827" height="479" alt="Screenshot 2025-08-29 103140" src="https://github.com/user-attachments/assets/8839b08a-d2d3-4359-8607-155c74fa55e4"/>
</p>
<p>
 - browse(...)
 - Go to your C drive
 - PHP folder
 - php.cgi
   <img <img width="831" height="453" alt="Screenshot 2025-08-29 103150" src="https://github.com/user-attachments/assets/56aebcef-9bc4-45c1-9f6f-373aea8ed796" />
</p>
<br />



<strong> 12. Reload IIS (Open ISS, Stop and Start the server) </strong>
- The restart button can be found on the right sider of the window
<p>
  <img <img width="824" height="483" alt="Screenshot 2025-08-29 103200" src="https://github.com/user-attachments/assets/12cf94b7-687e-4447-ae9d-3f20969f3cd2" />
</p>
<p>
</p>
<br />


<strong> 13. Download and install osTicket</strong>
- From the osTicket-Installation-Files unzip the (osTicketv1.15.8)
<p>
  <img <img width="622" height="462" alt="Screenshot 2025-08-29 103214" src="https://github.com/user-attachments/assets/0ac5dfc6-e328-42f7-b732-6594b18443f9"/>
</p>
<p>
 - After extracting the folder, click on the folder and then copy the "upload" folder into "c: inetpub\wwwroot"
    - open file explorer 
    - C drive
    - inetpub
    - wwwroot
</p>
 <img <img width="835" height="515" alt="Screenshot 2025-08-29 103228" src="https://github.com/user-attachments/assets/d72e2049-2e03-4812-bc35-6868603ce878"/>
 
 - Within "c: inetpub\wwwroot", Rename "upload" to "osTicket"

<img width="826" height="420" alt="Screenshot 2025-08-29 103241" src="https://github.com/user-attachments/assets/925e3cf2-b5fa-4a69-ba00-122dcfc0e0fd" /> 
<br />



<strong> 14. Reload IIS (Open ISS, Stop and Start the server) </strong>
- The restart button can be found on the right sider of the window
<p>
  <img <img width="824" height="486" alt="Screenshot 2025-08-29 103253" src="https://github.com/user-attachments/assets/d7893f70-25e2-4951-9548-fff17e3d88af" />
</p>
<p>
</p>
<br />



<strong> 15. Launch osTicket </strong>
- On the left hand side of IIS, Expand on the VM name > Sites > Default Website > osTicket
- click on the browse *:80(http)
<p>
  <img <img width="830" height="479" alt="Screenshot 2025-08-29 103327" src="https://github.com/user-attachments/assets/19e0f9e7-991c-4883-aaf5-8c4d3f0b48d4"/>
</p>
<p>
 - This should then lead to your browser opening osTicket
</p>
<img width="828" height="680" alt="Screenshot 2025-08-29 103339" src="https://github.com/user-attachments/assets/96b7f529-859e-405c-92de-04a6e6fade6e"/>

<br />



<strong> 16. Enable extensions </strong>
- open IIS > sites > Default > osTicket
- Double-click PHP manager
<p>
  <img <img width="830" height="479" alt="Screenshot 2025-08-29 103352" src="https://github.com/user-attachments/assets/9c9855e0-c045-4425-870f-2e61e58bc16c"/>
</p>
<p>
 - Click "Enable or disable an extension"

 - Enable: php_imap.dll
 - Enable: php_intl.dll
 - Enable: php_opache.dll
</p>
<img width="826" height="530" alt="Screenshot 2025-08-29 103408" src="https://github.com/user-attachments/assets/0ef5f5f5-ac73-46bd-ba28-c145afbdba44"/>

<br />



<strong> 17. Refresh osTicket </strong>
- Refresh the osTicket site in your browser, some extensions will now appear active 
<p>
  <img <img width="826" height="679" alt="Screenshot 2025-08-29 103418" src="https://github.com/user-attachments/assets/68cfcad5-9d52-49d3-822f-d71b253ff7ba"/>
</p>
<p>
</p>
<br />


<strong> 18. Change to ost-config.ph </strong>
- Rename: ost-config.php
- From: C:\inetpub|wwwrootlosTicket\includelost-sampleconfig.php
-To: C. linetpubiwwwrootlos Ticketinclude lost-config.php
- rename "ost-sampleconfig.ph" to "ost-config.ph"

<p>
  <img <img width="830" height="424" alt="Screenshot 2025-08-29 103431" src="https://github.com/user-attachments/assets/0c095ed5-362c-43ed-b644-65ab4104351b"/>
</p>
<p>
</p>
<br />


<strong> 19. Change ost-config.ph permissions </strong>
- Change ost-config.php permissions by right clicking and selecting
- Properties > Security > Advance > Disable inheritance
- Disable inhertiance > Remove All
<p>
  <img <img width="769" height="523" alt="Screenshot 2025-08-29 103443" src="https://github.com/user-attachments/assets/842059ab-be72-42ff-a3bd-010ea81094c4"/>
</p>
- New Permissions > Everyone > All
-Go to add > select prinicpal > Everyone > Clcik full access > apply > OK

<p>
  <img <img width="770" height="526" alt="Screenshot 2025-08-29 103454" src="https://github.com/user-attachments/assets/3a9bc10b-feda-4814-bd40-416774f8111a" />
</p>
<br />


<strong> 20. Continue osTicket installation</strong>
- Continue the osTicket installer on your browser by filling the first half of the page
<p>
  <img <img width="827" height="678" alt="Screenshot 2025-08-29 103510" src="https://github.com/user-attachments/assets/103c525b-f306-4c4b-86e2-b4c8a5836413" />
</p>
<p>
</p>
<br />

<strong> 21. Download and install Heidi SQL from the osTicket-Installation-Files </strong>
<p>
  <img <img width="605" height="466" alt="Screenshot 2025-08-29 103522" src="https://github.com/user-attachments/assets/0403a2ec-0236-4d8e-b542-c7ab7f0dda60" />
 />
</p>
- Open Heidi SQL and create a new version a new session
-Fill in username and password as (root)
- Then click open
<p>
 <img width="690" height="493" alt="Screenshot 2025-08-29 103535" src="https://github.com/user-attachments/assets/12e43958-60f3-416b-9c8f-b34c10767798"/>

</p>
<br />


<strong> 22. Create new database </strong>
- On the left side of the window, right click on "Unnamed" and click create new database and name it "osTicket"
<p>
  <img <img width="827" height="535" alt="Screenshot 2025-08-29 103547" src="https://github.com/user-attachments/assets/136fa14c-7684-47fa-9ff4-902c7dba6c7b" />
</p>
<p>
</p>
<br />


<strong> 23. Finish signing in database settings </strong>
- Then go back to your osTicket browser and fill up the missing credentials
- Install Now
<p>
  <img <img width="822" height="375" alt="Screenshot 2025-08-29 103601" src="https://github.com/user-attachments/assets/1ba19c00-c60e-4eb2-a416-a89f02091549"/>
</p>
<p>
</p>
<br />



<strong> 24. Finalize osTicket installation</strong>
<p>
  <img <img width="732" height="575" alt="Screenshot 2025-08-29 103614" src="https://github.com/user-attachments/assets/e6123fbc-ae2d-4251-a943-f2f810cdc506" />
</p>
<p>
 - Congrats! You just installed osTicket!
</p>
<br />


