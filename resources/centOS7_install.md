---
layout: default
course_number: CS350
title: Resources
---

This page contains a step-by-step guide through the installation of CentOS 7 and CLion.

### Install VMWare Player (or Fusion)

Not currently covered by this guide.


### Installing CentOS 7

**Step 1:** Boot Virtual machine from CentOS installation media.  
Select the "Install CentOS 7" option and press "Enter"
<br>
![image](centOS_images/step01.png)

===============================================================

**Step 2:** Press "Enter" at this screen
<br>
![image](centOS_images/step02.png)

===============================================================

**Step 3:** Click on "Software Selection" in the bottom right corner.
<br>
![image](centOS_images/step03.png)

===============================================================

**Step 4:** In the left-hand pane, select the "GNOME Deskop".
<br>
![image](centOS_images/step04.png)

===============================================================

**Step 5:** In the right-hand pane, scroll down and select "Development Tools".
Click "Done" in the top left-hand corner.
<br>
![image](centOS_images/step05.png)

===============================================================

**Step 6:** Click on "Installation Destination". It will likely have warning icon overlay.
<br>
![image](centOS_images/step06.png)

===============================================================

**Step 7:** Make sure your virtual hard disk drive is selected and has a checkmark. 
 Click "Done" in the top left-hand corner.
<br>
![image](centOS_images/step07.png)

===============================================================

**Step 8:** Verify that the warning overlay has disappeared from the "Installation Destination".
<br>
![image](centOS_images/step08.png)

===============================================================

**Step 9:** Click on "Network & Host Name".
<br>
![image](centOS_images/step09.png)

===============================================================

**Step 10:** Verify that you have an Ethernet adapter selected in the left-hand pane.
<br>
![image](centOS_images/step10.png)

===============================================================

**Step 11:** Click the ON/OFF toggle to enable your Ethernet adapater.
Click "Done" in the top left-hand corner.
<br>
![image](centOS_images/step11.png)

===============================================================

**Step 11.5:** Click "Being Installation".
<br>
![image](centOS_images/step09.png)

===============================================================

 **Step 12:** Click on "Root Password".
<br>
![image](centOS_images/step12.png)

===============================================================

**Step 13:** Set a root password (REMEMBER THIS PASSWORD!!!)
Click "Done" in the top left-hand corner.
<br>
![image](centOS_images/step13.png)

===============================================================

**Step 14:** Click "User Creation"
<br>
![image](centOS_images/step14.png)

===============================================================

**Step 15:** Type in your preferred username and password. 
This password need not be the same as the root password previously set.
Click "Done" in the top left-hand corner.
<br>
![image](centOS_images/step15.png)

===============================================================

**Step 16:** Wait patiently while the OS installs.
<br>
![image](centOS_images/step16.png)

===============================================================

**Step 17:** When the installation is complete, click the "Roboot" button.
<br>
![image](centOS_images/step17.png)

===============================================================

**Step 18:** When prompted, enter a "1" to begin the license manager.
<br>
![image](centOS_images/step18.png)

===============================================================

**Step 19:** Enter a "2" to mark your selection in the license manager.
<br>
![image](centOS_images/step19.png)

===============================================================

**Step 20:** Enter a "c" to accept the license.
<br>
![image](centOS_images/step20.png)

===============================================================

**Step 21:** Enter another "c" to continue booting the operating system.
<br>
![image](centOS_images/step21.png)

===============================================================

**Step 22:** Click the username that you previously created.
<br>
![image](centOS_images/step22.png)

===============================================================

**Step 23:** Enter the password that you created for the user (not the root password)
and click the "Sign In" button.
<br>
![image](centOS_images/step23.png)

===============================================================

**Step 24:** Select your language and click "Next"
<br>
![image](centOS_images/step24.png)

===============================================================

**Step 25:** Select your keyboard layout and click "Next". 

<br>
![image](centOS_images/step25.png)

===============================================================

**Step 26:** You should now be DONE installing CentOS 7.
Click the "Start using CentOS Linux" button to continue.
<br>
![image](centOS_images/step26.png)

===============================================================

===============================================================

===============================================================



### Installing Development Tools and Clang

**Step 1:** Click the "Applications" menu in the top-left corner, find and run 
the "Terminal" application.
<br>
![image](centOS_images/step27.png)

===============================================================

**Step 2a:** Determine if you already have the development tools installed by typing
```which make```
at the command line and hit enter. If you see the response ```/usr/bin/make``` then
 you already have most of the development tools installed.  Skip down to Step #5.
<br>
![image](centOS_images/step28.png)

===============================================================

**Step 2b:** When typing ```which make```, if the response contains 
the phrase ```no make in ...``` and looks like the screenshot below
then you don't have the development tools properly installed. Continue
to Step #3.
<br>
![image](centOS_images/step29.png)

===============================================================

**Step 3:** In the terminal, type ```su``` to switch users. The ```su``` 
command will make you the root user. Enter the **root password** when prompted.
<br>
![image](centOS_images/step30.png)

===============================================================

**Step 4:** As the root user, type the following:
```yum groupinstall 'Development Tools'``` and hit enter.
Follow the prompts, enter a ```y``` for "Yes" when required.
When this command completes, the development tools should be 
installed. You can verify success by re-running the command from 
Step 2a.
<br>
![image](centOS_images/step31.png)

===============================================================

**Step 5:** Use the terminal to install clang. If you are not 
already the root user, type ```su``` to switch users to the root user.
Enter the **root password** when prompted.
As the root user, type the following to install clang: 
```yum install clang```.
Follow the prompts, enter a ```y``` for "Yes" when required.
When this command completes, clang should be installed.
<br>
![image](centOS_images/step32.png)

===============================================================

===============================================================

===============================================================



### Installing CLion


**Step 1:** Download CLion from the [jetbrains website](https://www.jetbrains.com/clion/download/#section=linux).
Save the file to your Desktop.
<br>
![image](centOS_images/step33.png)

===============================================================

**Step 2:** Open the Terminal application. Type ```cd Desktop``` to change directories
to your Desktop directory.  If you are not already the root user, 
type ```su``` to switch users to the root user.
Enter the **root password** when prompted.
<br>
![image](centOS_images/step34.png)

===============================================================

**Step 3:** As the root user, type the following:
```tar -xzf CLion-2017.2.2.tar.gz -C /opt```.
This will unpack the archive file into the ```/opt``` directory.
<br>
![image](centOS_images/step35.png)

===============================================================

**Step 4:** Type ```exit``` to logout of the root user account.
<br>
![image](centOS_images/step36.png)

===============================================================

**Step 5:** Type the following to start CLion for the first time:
```/opt/clion-2017.2.2/bin/clion.sh```.
<br>
![image](centOS_images/step37.png)

===============================================================

**Step 6:** Select "Do not import settings" and click "ok".
<br>
![image](centOS_images/step38.png)

===============================================================

**Step 7:** Enter the username and password for your free JetBrians
student account. Click "Activate" to continue.
<br>
![image](centOS_images/step39.png)

===============================================================

**Step 8:** Select a theme and click "Next".
<br>
![image](centOS_images/step40.png)

===============================================================

**Step 9:** Leave these settings at their default values and click "Next".
<br>
![image](centOS_images/step41.png)

===============================================================

**Step 10:** Leave these settings at their default values and click "Next".
<br>
![image](centOS_images/step42.png)

===============================================================

**Step 11:** Leave these settings at their default values and click "Next".
<br>
![image](centOS_images/step43.png)

===============================================================

**Step 12:** Ensure the checkbox labeled "Create a desktop entry ..." is selected.
Click "Start using CLion".
<br>
![image](centOS_images/step44.png)

===============================================================

**Step 13:** Admire your success and click the X to close CLion for now.
<br>
![image](centOS_images/step45.png)

===============================================================

**Step 14:** Cleanup your desktop by deleting the archive file. 
Type the following:
```rm CLion-2017.2.2.tar.gz```
<br>
![image](centOS_images/step46.png)

===============================================================

**Step 15:** From now on, you should be able to start CLion from 
the "Applications -> Programming" menu.
<br>
![image](centOS_images/step47.png)

===============================================================