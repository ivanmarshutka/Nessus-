# Nessus-
Nessus Vulnerability Scan

Register for Nessus® Essentials Activation code at tenable.com
Download Tenable Nessus® Essentials  - Install - Save the redirected URL - Press Connect via SSL - Log in - Use Activation code that you received on email 

Go to Windows 10 Virtual Machine 
Go to searchbar and open Windows Defender Firewall
Go to Windows Defender Firewall Properties - Turn off firewall state for Domain, Private and Public Profiles - Apply
Open Command Prompt use ipconfig command to lookup machine`s IP address.  

Go to host Windows 10 machine open Command Prompt - use ping command followed by the IP of target VM to check connectivity 

Uncredentialed Scan
Go to Nessus host web page 
Create a new scan - Basic Network Scan - Name it - Put target VM`s IP in a target section - Save - Back to My Scans - Press  Launch 

Windows Settings for credentialed Nessus Essential vulnerability scan:
Go to Windows services - Enable remote registry - set to automatic, apply and start the process 
Go to Advanced sharing settings - check if file and printer sharing is on
Go to User account control - if VM`s Network adapter is set to bridged - scroll to never notify, VM`s Network adapter is set to NAT leave at default
Go to Registry editor - HKEY_LOCAL_MACHINE - Software - Microsoft - Windows - create DWORD (32-bit) Value , name it LocalAccountFilterPolicy - double left click , set value to 1 
Restart VM

Credentialed Scan 
Nessus hostpage
Checkmark your scan 
Go to more - Configure - Credentials - Windows - Use credentials for the scanning target machine ( Command Prompt whoami command - Leave Global Credential Settings at default - Save - Back to My Scans page - Press Launch 
