# Install-WSL-2-in-Windows-11-Windows-10
WSL 2 is eligible for Windows 11, Windows 10:

* For x64 systems: Version 1903 or higher, with Build 18362 or higher
* For ARM64 systems: Version 2004 or higher, with Build 19041 or higher

-->To check your version and build number, select Windows logo key + R, type winver, select OK


Installation: 

1. Enable the Windows Subsystem for Linux:

   > dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart

2. Enable Virtual Machine feature:
   
   > dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

3. Download the Linux kernel update package:
   
   https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi
   
4. Microsoft Store: Install your Linux distribution of choice. Launch it to create user.

5. Set your distribution version to WSL 1 or WSL 2:
   
   > wsl --list --verbose
   
   > wsl --set-version distributionNameHere versionNumberHere
   
     For example, in case of Ubuntu-20.04, enter [wsl --set-version Ubuntu-20.04 2] 

   > wsl --set-default-version 2
   

