# Install-WSL-2-in-Windows-11-Windows-10

Installation: 

1. Enable the Windows Subsystem for Linux:

   dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart

2. Enable Virtual Machine feature:
   
   dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

4. Microsoft Store: Install your Linux distribution of choice. Launch it to create user.

3. Download the Linux kernel update package:

   https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi

5. Set your distribution version to WSL 1 or WSL 2:
   
   > wsl --list --verbose
   
   > wsl --set-version <distribution name> <versionNumber>
   
     For example, in case of Ubuntu-20.04, enter wsl --set-version Ubuntu-20.04 2 

   > wsl --set-default-version 2
