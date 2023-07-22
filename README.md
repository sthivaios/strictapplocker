# strictapplocker
Strict Policies For Windows App Locker

# What is AppLocker?
AppLocker is a feature in Windows PRO editions.
It allows Administrators to configure what script or executables can be run and which are blocked.
It is very useful and if configured correctly, it can prevent malware from being run.
The feature can be accessed by opening "Group Policy Management" and on the side panel, navigating
to Local Computer Policy > Computer Configuration > Windows Settings > Security Settings > Application
Control Policies > AppLocker.
There, you can configure specific polices to allow or block apps from running depending on specific criteria.

# What is "strictapplocker"
Scrictapplocker are 8 policies preconfigured to allow a very limited range of applications
and scrpits to be run.
By right clicking the AppLocker section in Group Policy Management, in the path described above, you can
import a policy. Strictapplocker are a set of 8 polices that are as the name implies strict, and allow only
the following to run :
1) All executable files that are signed by any publisher
2) All Windows installers (.msi files) that are signed by Microsoft Corporation

The strictapplocker policies block the following from running :
1) All .com files *(similar to .exe files)*
2) All .scr files *(screen saver files usually used for malware)*
3) All .bat files *command line scripts)*
4) All .cmd files *(like .cmd files, command line scripts)*
5) All .vbs files *(visual basic scripts usually used to spread worms)*
6) All .ps1 files *(powershell scripts that are often used for malware)*

# How do I configure these policies on my computer?
Steps:
1) Download the strictapplocker.xml file
2) Open "Group Policy Management" on your Windows computer
3) Navigate to Local Computer Policy > Computer Configuration > Windows Settings > Security Settings > Application
Control Policies
4) Right click on AppLocker
5) Choose "Import Policy"
6) Select the strictapplocker.xml file and import it
7) You should get a message informing you that the import was successful
8) You have now succesfully configured stricapplocker!

*If you are still having difficulty setting up strictapplocker, watch the video below*
https://github.com/sthivaios/strictapplocker/assets/109022579/f15a249f-46d6-47f4-b24c-93bbc9fb777e

# Notes
Keep in mind, strictapplocker is VERY strict.
This means that even files like .mp4 and .jpg will be blocked.
