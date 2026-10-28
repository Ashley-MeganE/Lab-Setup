<h1 align="center"> Cybersecurity Lab Environment Setup </h1>

### **Objective**

The purpose of this project is the setup and installation of VirtualBox and Kali Linux on my Windows 10 PC, and the creation of an isolated NAT Network for both.

**Applications used:**  
• Oracle VirtualBox  
• Kali Linux  
• 7Zip (previously installed)

### **Installations and Network Set Up**
To begin this set up, I downloaded VirtualBox from the official website which went smoothly. The application was easy to install.  Afterwards, IP set up was done successfully by going into the network settings and manually inputting the chosen IPv4 Prefix, 10.0.0.0/24 as seen in the screenshot below. 

<img width="1366" height="768" alt="virtualbox_network_ip" src="https://github.com/user-attachments/assets/735c1d65-417f-4677-820e-fa2f41b82f7b" />  

<br>
<br>
Next, I downloaded Kali for VirtualBox, which took some time as it's a heavier app. After extracting with 7Zip and opening the VM in VirtualBox, I logged in using the default username and password (kali, kali). In the network settings, I set Wired Connection 1 to Manual and edited it to reflect the desired IP, 10.0.0.2 with a gateway of 10.0.0.1 with a DNS of 8.8.8.8 (Google Public DNS) as seen in the screenshots below.

<br>
<br>

<img width="1280" height="674" alt="VirtualBox_kali-linux-SS1" src="https://github.com/user-attachments/assets/7f44f00e-82d7-42e7-be83-8fdbc05bb6ab" />  
<br> 
<br>
After this, I tested to see if Kali had internet access by searching for something random on its Firefox, which in this case was red velvet.  <br>
<br>

<img width="1280" height="674" alt="virtualbox_kali-linux--internet-proof" src="https://github.com/user-attachments/assets/da2be0e0-f686-41bc-a848-804caeb5a86d" />


Once I confirmed that Kali has internet access, I shut the virtual machine down and took a snapshot. 

### **Problems encountered:**  
None, as I have completed installations like this before and know my way around Kali Linux. 

### **What I Learned:**
* VM snapshots as an operational clean slate. This establishes a backup to counter accidental configuration drift, corrupted dependencies, or system breaks during high-risk exercises.  

* NAT Network vs regular NAT. With NAT Network the Kali machine can reach out to the internet to download tools, and any target VMs added to this network in the future will be instantly discoverable by the Kali instance.

* Learned how to design a segmented network topology that allows Kali outbound access to the public internet for tool installations while keeping the host machine's primary interface decoupled from potential virtual network exposure.

## **Author and Lab Information**
**Ashley-Megan Ikhialose Ehiede**  

**Project Information:**  
Program Name: Cybersecurity at NetworkWalks | Week: 01 | Project: Cybersecurity & Pentesting Lab Setup

