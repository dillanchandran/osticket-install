<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://youtu.be/5V32I8wI92E)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machine)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Machine Setup
- Install Web Server
- Install PHP
- Item 4
- Item 5

<h2>Installation Steps</h2>

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 8 54 53 AM" src="https://github.com/user-attachments/assets/6b198669-f0cd-4e36-a8af-406abe20ac75" />
</p>
<p>
In the Azure portal, create a virtual machine by searching 'virtual machine' in the Azure search box and select create 

<p>
<img width="400" alt="Screen Shot 2024-12-24 at 3 41 57 PM" src="https://github.com/user-attachments/assets/364cce9f-427d-4265-85f2-8579a173ed05" />
</p>

From there the configuration steps will show as pictured above. Complete all the required fields (red asterix)

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 9 00 09 AM" src="https://github.com/user-attachments/assets/49f08616-054e-4441-bf75-6a2d0e0a9343" />
</p>

Make sure you remember the username and password you use for the administator account as that is what we will use to login to the virtual machine

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 9 01 11 AM" src="https://github.com/user-attachments/assets/76358a3e-8cf5-43aa-a54b-54859b040f3d" />
</p>

For the 'Image' field select Windows 10 Pro as that will be the operating system we will be using

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 9 01 58 AM" src="https://github.com/user-attachments/assets/38eeeaef-43f5-4cd4-bffb-aec0957ba7be" />
</p>

Ensure the 'Allow selected ports' option is selected for 'Public inbound ports' and the RDP (3389) is selected for the inbound port as that will allow for the virtual machine to be accessible

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 9 02 41 AM" src="https://github.com/user-attachments/assets/b3248b43-f795-4758-aeb4-b58dcca76dd0" />
</p>

After all required fields are filled select 'Review + create' at the bottom of the screen for the virtual machine to be deployed

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 9 26 52 AM" src="https://github.com/user-attachments/assets/57c3ac6d-38ff-4f6d-bae1-e65ca61b6ec7" />
</p>

Once deployed make your way back to the virtual machine page on Azure. Scroll left on the newly created virtual machine until you see it's public IP address and copy it

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 9 32 55 AM" src="https://github.com/user-attachments/assets/8b5fea1e-a9c6-4d08-892a-e31746609171" />
</p>

Open up Remote Desktop/Windows App depending on the operating system you are using and select 'Add PC'

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 9 38 44 AM" src="https://github.com/user-attachments/assets/a8073733-4a76-4337-bc9c-df2cd8906844" />
</p>

A dialog box will open up and in the 'PC name' field you will paste the public IP address on your vitual machine. You can also fill the 'Friendly name' field to name the virtual machine in Remote Desktop/Windows App. Once complete click add at the bottom of the dialog box

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 9 57 26 AM" src="https://github.com/user-attachments/assets/2777e5a1-ad1f-4a08-91f1-21a79529439c" />
</p>

Once added double click the added PC which will open up a dialog box. Here you will input the administrator account information created in virtual machine configuration steps in the username and password field 

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 10 38 25 AM" src="https://github.com/user-attachments/assets/4539aedd-5b5a-4635-b37b-fe95d0776a00" />
</p>

When logged in download all the files needed to install osTicket on the vitrual machine. Here is the link to download those files https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD

<p>
<img width="541" alt="Screen Shot 2024-12-25 at 10 39 31 AM" src="https://github.com/user-attachments/assets/bdeb66c5-8787-4fc8-a78d-12e82c6e5345" />
</p>

Once downloaded extract all files for use later

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 11 34 54 AM" src="https://github.com/user-attachments/assets/88f904ba-15b7-4281-a955-d005bc54745a" />

</p>

To install the web server, open control panel

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 11 37 57 AM" src="https://github.com/user-attachments/assets/ade5bd41-5fb7-4f46-8c9b-7d1413b5193b" />
</p>

Click 'Uninstall a program'

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 11 38 14 AM" src="https://github.com/user-attachments/assets/086f5c06-ce91-47de-babb-132dbdfe9aba" />
</p>

Select 'Turn windows features on or off'

</p>

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 11 39 46 AM" src="https://github.com/user-attachments/assets/7b389813-7b8a-4ea6-8934-bfe56062d89a" />
</p>

Check and expand 'Internet Information Service'

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 11 45 37 AM" src="https://github.com/user-attachments/assets/d7913935-3412-40ff-8e81-10bded287bbd" />
</p>

Then expand the folders 'World Wide Web Services', 'Application Development Features', check the folder 'CGI' and click OK. Enabling Internet Information Service and CGI will allow for osTicket to function properly on the web server in the virtual machine


<p>
<img width="400" alt="Screen Shot 2024-12-25 at 11 49 23 AM" src="https://github.com/user-attachments/assets/e28336c6-b9f6-4bf4-be9b-6235fcf3a6e1" />
</p>

PHP needs tto be installed as that is what osTicket is coded with. To do so, head back to the osTicket installation files we downloaded and expanded. Once there, double click the 'PHPformanagerIIS_V1.5.0' file

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 11 52 32 AM" src="https://github.com/user-attachments/assets/2cbf6d2f-cd75-4d9d-9de2-e44a195af30d" />
</p>

An installation wizard will pop up. Select next agree to the license agreement to install PHP. Once completed you can close the wizard

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 11 57 48 AM" src="https://github.com/user-attachments/assets/f1a1c18a-e8f2-4172-b002-627599b8418e" />
</p>

Next the IIS rewrite module will be downloaded. This will allow for more user-friendly URLs to be created when using osTicket. Head back to the osTicket installation files we downloaded and expanded. Once there, double click the 'rewrite_amd64_en-US' file.

<p>
<img width="396" alt="Screen Shot 2024-12-25 at 11 59 26 AM" src="https://github.com/user-attachments/assets/9f671207-8b10-4b8b-8dda-78ad9473d2c6" />
</p>

An installation wizard will pop up. Accept the license agreement and click 'Install'. Once completed select 'Finish'

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 12 06 22 PM" src="https://github.com/user-attachments/assets/d68930ca-21fa-440d-9fab-e6c61a5d48be" />
</p>

Next a PHP folder needs to be created in the C drive along with adding the necessary executable file to allow for PHP to be intergrated onto the system. Find the 'Windows (C:)' option in the 'File Manager' and select it to open the C drive.

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 12 15 29 PM" src="https://github.com/user-attachments/assets/57cc51e7-b8ce-4cb6-aedc-e5ad0cbc519e" />
</p>

Once the C drive is opened, left click to open up the menu, hover over 'New' and select 'Folder'

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 12 16 31 PM" src="https://github.com/user-attachments/assets/46a64063-2200-474f-8752-6399e7559ab2" />
</p>

Then rename the newly created folder to 'PHP' by left clicking it and selecting 'Rename'

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 12 19 57 PM" src="https://github.com/user-attachments/assets/c18746b3-7300-4395-9652-4b5dbb8e1d15" />
</p>

After that open up file explorer by left clicking the file explorer icon at the bottom and select 'File Explorer'

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 12 25 10 PM" src="https://github.com/user-attachments/assets/d5891e0d-0612-4163-a4d5-0adb318ea07a" />
</p>

In the file explorer, head back to the osTicket installation files folder and extract the 'php-7.3.8-nts-Win32-VC15-x86' zipped file

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 12 27 23 PM" src="https://github.com/user-attachments/assets/f03c0e38-4239-470f-9164-1df6dfa41bb0" />
</p>
<p>
<img width="400" alt="Screen Shot 2024-12-25 at 12 27 47 PM" src="https://github.com/user-attachments/assets/93c1c4ad-f29e-4a57-a208-f140e0623af9" />

</p>

When extracting ensure the extraction destination will be the newly created PHP file in the C drive by clicked browse and selecting the newly created PHP file in the C drive

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 12 50 58 PM" src="https://github.com/user-attachments/assets/3de5239d-e0f5-486b-bdca-f679f4563fdd" />
</p>

When selected, click 'Extract'

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 12 50 58 PM" src="https://github.com/user-attachments/assets/3de5239d-e0f5-486b-bdca-f679f4563fdd" />
</p>

When selected, click 'Extract'

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 12 59 31 PM" src="https://github.com/user-attachments/assets/cebe464b-b322-4935-b113-edb92e182b53" />
</p>

Next the Microsoft Visual C++ Reddistributable Package will be downloaded. This will allow for osTicket to fun all functions that rely on certain C++ libraries. Head back to the osTicket installation files we downloaded and expanded. Once there, double click the 'VC_redist.x86' file


<p>
<img width="400" alt="Screen Shot 2024-12-25 at 1 12 23 PM" src="https://github.com/user-attachments/assets/cc18840f-baa3-46bc-be1b-af78226c04e3" />
</p>

An installation wizard will pop and, agree to the license agreement and click 'Install'. Close once complete

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 1 17 41 PM" src="https://github.com/user-attachments/assets/fed68b81-bf3e-4e83-9164-0c06ca8eceec" />
</p>

Next MySQL will be downloaded. This will be the database management system for osTicket. Head back to the osTicket installation files we downloaded and expanded. Once there, double click the 'mysql-5.5.61-win32' file

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 1 26 04 PM" src="https://github.com/user-attachments/assets/a0667fea-17cd-4c24-8315-ac48f226b23d" />
<img width="400" alt="Screen Shot 2024-12-25 at 1 26 21 PM" src="https://github.com/user-attachments/assets/6b8618cf-75ac-45f2-891c-1f43256c1dca" />
<img width="400" alt="Screen Shot 2024-12-25 at 1 26 48 PM" src="https://github.com/user-attachments/assets/a3608ae5-befe-4a1e-8c1e-14a36edd0f92" />
</p>

On the installation wizard select 'Next', agree to the license agreenement and select 'Next' again. Click the setup type 'Typical'. Then click 'Install'. 

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 1 28 14 PM" src="https://github.com/user-attachments/assets/587f6502-2531-4b55-889d-0c80e1dc2c6a" />
</p>

When installed ensure 'Launch the MySQL Instance Configuration Wizard' is checked and click 'Finish'

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 9 21 24 PM" src="https://github.com/user-attachments/assets/232dc59e-7a57-4811-afe8-6c1f218a0bdf" />
</p>

A configuration wizard will pop up, click 'Next'

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 9 24 44 PM" src="https://github.com/user-attachments/assets/3e4109df-d939-4b60-8a8b-9075181e1cbf" />
</p>

Change the configuration type to 'Standard configuration' and click next again

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 9 26 34 PM" src="https://github.com/user-attachments/assets/46443f4f-ef46-425b-8fbb-5090bc946217" />
</p>

Keep the setting the same on the next page and click 'Next'. You will then need to create your root password for your MySQL server instance

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 9 28 04 PM" src="https://github.com/user-attachments/assets/532c0352-a843-4632-ad7a-5ebd5b0fda76" />
</p>

Then click 'Execute' to start the configuration. Once complete click 'Finish' to close the wizard

<p>
<img width="400" alt="Screen Shot 2024-12-25 at 9 35 56 PM" src="https://github.com/user-attachments/assets/8e854e82-a4ad-4cd6-be17-f8cc066703d8" />
</p>

Next the PHP manager installed and setup needs to be registered in IIS (Internet Information Services) and to do so IIS manager needs to be opened as an administrator. Search IIS in the botttom left search bar of the screen, then right click 'Internet Information Services (IIS) manager' and select 'Run as administrator'

<p>
<img width="400" alt="Screen Shot 2024-12-26 at 10 46 39 AM" src="https://github.com/user-attachments/assets/5099dc89-52b2-4687-831d-ac7fc1e50d8f" />
</p>

Once the Internet Information Services (IIS) manager opens, click on 'PHP Manager'

<p>
<img width="400" alt="Screen Shot 2024-12-26 at 10 47 30 AM" src="https://github.com/user-attachments/assets/edecac24-68a4-4f61-b4b9-1b0a31a54a86" />
</p>

On the PHP manager page, select 'Register new PHP version'

<p>
<img width="400" alt="Screen Shot 2024-12-26 at 10 48 47 AM" src="https://github.com/user-attachments/assets/6f6da11f-6125-4337-8044-45751a2c0b35" />
</p>

A file picker dialog box will pop up, click the button with 3 dots

<p>
<img width="573" alt="Screen Shot 2024-12-26 at 10 49 25 AM" src="https://github.com/user-attachments/assets/40b15e8f-a9dd-4134-baa8-320c48f01e3e" />
</p>

A dialog box prompting you to 'Select PHP executable file' will appear, locate the 'php-cgi' file which was added to the PHP folder in the C drive.  Select the 'php-cgi' file and click 'Open'

<p>
<img width="400" alt="Screen Shot 2024-12-26 at 10 48 47 AM" src="https://github.com/user-attachments/assets/6f6da11f-6125-4337-8044-45751a2c0b35" />
</p>

Then press 'OK' on the file picker dialog

<p>
<img width="400" alt="Screen Shot 2024-12-26 at 11 04 57 AM" src="https://github.com/user-attachments/assets/a192e23d-10b7-476b-b012-1f80f0caf733" />
</p>

The server now needs to be restarted. On the Internet Information Services (IIS) manager, select the server (under connections on the left side). Once the server is selected, click 'Restart' on the right side

<p>
<img width="400" alt="Screen Shot 2024-12-26 at 11 31 05 AM" src="https://github.com/user-attachments/assets/f407f862-372d-4dd4-8749-794907918dc6" />
<img width="400" alt="Screen Shot 2024-12-26 at 11 31 13 AM" src="https://github.com/user-attachments/assets/9acc354c-c3cf-43ad-9c48-716c165637cb" />
</p>

osTicket can now be added to the web server. Head back to the osTicket installation files we downloaded and expanded. Once there, right click the 'osTicket-v1.15.8' zipped file and click 'Extract all'. When the extraction dialog box pops up, ensure the 'Show extracted files when complete' is checked and select 'Extract'

<p>
<img width="400" alt="Screen Shot 2024-12-26 at 11 55 15 AM" src="https://github.com/user-attachments/assets/dc1c821d-0c51-423c-ae72-57afdf8d0e70" />
<img width="400" alt="Screen Shot 2024-12-26 at 11 55 25 AM" src="https://github.com/user-attachments/assets/0e8fd85e-3ec5-4b7e-b6d8-f777a246d402" />
<img width="400" alt="Screen Shot 2024-12-26 at 11 55 32 AM" src="https://github.com/user-attachments/assets/1f73eb96-28b8-4061-8aba-bad20a78212a" />
</p>

Once the extraction is complete, a second file explorer will appear with the extracted files. Move the newly opened file explorer to a side. On the inital file explorer, head over to the C drive then select 'inetpub', then 'wwwroot'

<p>
<img width="400" alt="Screen Shot 2024-12-26 at 12 00 58 PM" src="https://github.com/user-attachments/assets/8eeb89ac-7fef-44db-b08b-2b21d669f868" />
</p>

On the second file explorer with the extracted 'osTicket-v1.15.8' files, drag and drop the 'upload' folder into the 'wwwroot' folder

<p>
<img width="400" alt="Screen Shot 2024-12-26 at 12 02 54 PM" src="https://github.com/user-attachments/assets/b0e4f9bd-c179-42db-b384-16413e513775" />
</p>

Rename the newly moved 'upload' folder in the 'wwwroot' folder to 'osTicket'

<p>
<img width="400" alt="Screen Shot 2024-12-26 at 11 04 57 AM" src="https://github.com/user-attachments/assets/a192e23d-10b7-476b-b012-1f80f0caf733" />
</p>

The server now needs to be restarted again. On the Internet Information Services (IIS) manager, select the server (under connections on the left side). Once the server is selected, click 'Restart' on the right side If you closed the Internet Information Services (IIS) manager, Search IIS in the botttom left search bar of the screen, then right click 'Internet Information Services (IIS) manager' and select 'Run as administrator'

<p>
<img width="400" alt="Screen Shot 2024-12-26 at 10 46 39 AM" src="https://github.com/user-attachments/assets/4108de6e-d2f5-4c31-b8e9-d6c649b1438d" />
</p>

Now open the osTicket website. In the connection section (left side) on the Internet Information Services (IIS) manager, expand 'Sites', 'Default Web Site' and select the 'osTicket' folder.

<p>
<img width="400" alt="Screen Shot 2024-12-26 at 12 31 09 PM" src="https://github.com/user-attachments/assets/529a09c1-ca04-48be-9491-04d6e5b64140" />
<img width="400" alt="Screen Shot 2024-12-26 at 12 31 38 PM" src="https://github.com/user-attachments/assets/254b4df0-432d-4010-aab1-59d700e86975" />
</p>

On the right side of the Internet Information Services (IIS) manager, click 'Browse *80 (http)' and the osTicket install website will pop up


<p>
<img width="400" alt="Screen Shot 2024-12-26 at 12 35 04 PM" src="https://github.com/user-attachments/assets/3c37b331-6c35-4b50-a94e-d75d33cbc40b" />
</p>

Certain recommended extensions are disabled which will be enabled in the following steps. Open up the Internet Information Services (IIS) manager again and whilst the osTicket folder is still selected, click 'PHP manager'

<p>
<img width="400" alt="Screen Shot 2024-12-26 at 12 51 26 PM" src="https://github.com/user-attachments/assets/4c85e7d6-966f-4cf3-93d9-4d2c09e773da" />
<img width="400" alt="Screen Shot 2024-12-26 at 12 53 40 PM" src="https://github.com/user-attachments/assets/c7decaea-24fe-4a7c-a4a0-db1b7485b93b" />
</p>

Once PHP manager has opened, click 'Enable or disable an extension'

<p>
<img width="300" alt="Screen Shot 2024-12-26 at 12 57 31 PM" src="https://github.com/user-attachments/assets/bb7f2c53-392a-48bf-980f-0ecbceecdc2a" />
<img width="300" alt="Screen Shot 2024-12-26 at 12 57 45 PM" src="https://github.com/user-attachments/assets/3e059cc8-f966-4017-8c21-f546cab28f57" />
<img width="300" alt="Screen Shot 2024-12-26 at 12 58 01 PM" src="https://github.com/user-attachments/assets/6f407892-db8c-45f7-9963-ff812ce886d6" />
</p>

in the PHP entensions folder enable php_imap.dll, php_intl.dll and php_opache.dll. To enable them, left click on the file and select 'Enable'


<p>
<img width="400" alt="Screen Shot 2024-12-26 at 11 55 15 AM" src="https://github.com/user-attachments/assets/dc1c821d-0c51-423c-ae72-57afdf8d0e70" />
<img width="400" alt="Screen Shot 2024-12-26 at 11 55 25 AM" src="https://github.com/user-attachments/assets/0e8fd85e-3ec5-4b7e-b6d8-f777a246d402" />
<img width="400" alt="Screen Shot 2024-12-26 at 1 08 09 PM" src="https://github.com/user-attachments/assets/bc14c142-ddc4-4e20-81b9-989881a8838c" />
<img width="400" alt="Screen Shot 2024-12-26 at 1 09 15 PM" src="https://github.com/user-attachments/assets/a0b8caea-0b3c-4194-b615-c0141e69332d" />
</p>

Next the placeholder php file that will hold the configuration settings needs to be activated aand given the ability to be accessed. To do this the 'ost-sampleconfig.php' file needs to be renamed to 'ost-config.php'. To find the 'ost-sampleconfig.php' file, head over to the C drive then select 'inetpub', then 'wwwroot', then 'osTicket' then 'include'

<p>
<img width="400" alt="Screen Shot 2024-12-26 at 1 10 25 PM" src="https://github.com/user-attachments/assets/1105ab91-0369-43e8-b774-10ec4389a692" />
<img width="200" alt="Screen Shot 2024-12-26 at 1 11 35 PM" src="https://github.com/user-attachments/assets/db5a298e-2b43-4f6f-a3a7-cca7469104df" />
<img width="123" alt="Screen Shot 2024-12-26 at 1 12 36 PM" src="https://github.com/user-attachments/assets/bf9d6f09-708d-468a-82b3-9330c9511e2a" />
</p>

From the include file you will find the 'ost-sampleconfig.php' file. Right click it, select 'Rename' and rename it to 'ost-config.php'

<p>
<img width="400" alt="Screen Shot 2024-12-26 at 5 06 54 PM" src="https://github.com/user-attachments/assets/5a685aa9-95b0-4de0-86e4-963107e930ef" />
</p>

Next, permissions need to be assigned for the 'ost-config.php' file to be accessible. Right click the 'ost-config.php' file and click 'Properties'

<p>
<img width="300" alt="Screen Shot 2024-12-26 at 5 09 27 PM" src="https://github.com/user-attachments/assets/21e5d496-3a29-4f19-8ff7-2447e54db61a" />
</p>

When the properties dialog box appears, select the 'Security' tab at the top and then click the 'Advanced' button



<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
