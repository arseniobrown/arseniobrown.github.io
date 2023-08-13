---
title: Installing Pfsense
author: Arsenio Brown
date: 2023-08-12 12:00:00 +0000  # Replace with today's date and time
categories: [Labs, Cybersecurity, Threat_Hunting]
tags: [Threat Hunting, Network Security, Firewall]
image:
  path: /assets/images/Projects/Threathuntinglab/installing-Pfsnes.png
  alt: Installing and Configuring Pfsense
---

  

## Installing Pfsense

  

Download Pfsense ISO file here  [Pfsense](https://www.pfsense.org/download/)

  

1. Click `Create a New Virtual Machine` on VMware Workstation Home Screen.
 ![2023-08-13 07_53_52-VMware Workstation.png](/assets/images/Projects/Threathuntinglab/2023-08-13%2007_53_52-VMware%20Workstation.png)
2. Make sure that "Typical (recommended)" is selected and click `Next`
![2023-08-13 07_59_52-New Virtual Machine Wizard.png](/assets/images/Projects/2023-08-13%2007_59_52-New%20Virtual%20Machine%20Wizard.png)
3. Click "Installer disc image file (iso)" then `Browse` and select your Pfsense ISO

![2023-08-13 08_05_23-New Virtual Machine Wizard.png](/assets/images/Projects/2023-08-13%2008_05_23-New%20Virtual%20Machine%20Wizard.png)
![2023-08-13 08_06_27-Browse for ISO Image.png](/assets/images/Projects/2023-08-13%2008_06_27-Browse%20for%20ISO%20Image.png)
![2023-08-13 08_08_40-Browse for ISO Image.png](/assets/images/Projects/2023-08-13%2008_08_40-Browse%20for%20ISO%20Image.png)
![2023-08-13 08_09_24-New Virtual Machine Wizard.png](/assets/images/Projects/2023-08-13%2008_09_24-New%20Virtual%20Machine%20Wizard.png)
4. Change the virtual machine name `Pfsense`
![2023-08-13 08_10_20-New Virtual Machine Wizard.png](/assets/images/Projects/2023-08-13%2008_10_20-New%20Virtual%20Machine%20Wizard.png)
![2023-08-13 08_13_13-Browse For Folder.png](/assets/images/Projects/2023-08-13%2008_13_13-Browse%20For%20Folder.png)
![2023-08-13 08_13_48-New Virtual Machine Wizard.png](/assets/images/Projects/2023-08-13%2008_13_48-New%20Virtual%20Machine%20Wizard.png)
![2023-08-13 08_14_18-New Virtual Machine Wizard.png](/assets/images/Projects/2023-08-13%2008_14_18-New%20Virtual%20Machine%20Wizard.png)
4. Click `Customize Hardware`
![2023-08-13 08_14_57-New Virtual Machine Wizard.png](/assets/images/Projects/2023-08-13%2008_14_57-New%20Virtual%20Machine%20Wizard.png)
5. Increase the memory to `2GB` and click `add`
![2023-08-13 08_15_42-Hardware.png](/assets/images/Projects/2023-08-13%2008_15_42-Hardware.png)
6. Add 5 network adapters and correspond them with a VMnet interface as shown below then click `Finish`

![2023-08-13 08_16_42-Add Hardware Wizard.png](/assets/images/Projects/2023-08-13%2008_16_42-Add%20Hardware%20Wizard.png)

![2023-08-13 08_19_57-Hardware.png](/assets/images/Projects/2023-08-13%2008_19_57-Hardware.png)
![2023-08-13 08_21_16-Hardware.png](/assets/images/Projects/2023-08-13%2008_21_16-Hardware.png)
![2023-08-13 08_21_43-New Virtual Machine Wizard.png](/assets/images/Projects/2023-08-13%2008_21_43-New%20Virtual%20Machine%20Wizard.png)
7.  The PfSense machine will be powered on, and you should proceed by accepting all the default settings before rebooting.

![2023-08-13 08_24_48-.png](/assets/images/Projects/2023-08-13%2008_24_48-.png)
![2023-08-13 08_25_31-.png](/assets/images/Projects/2023-08-13%2008_25_31-.png)
![2023-08-13 08_26_12-.png](/assets/images/Projects/2023-08-13%2008_26_12-.png)
![2023-08-13 08_27_39-.png](/assets/images/Projects/2023-08-13%2008_27_39-.png)
![2023-08-13 08_28_37-.png](/assets/images/Projects/2023-08-13%2008_28_37-.png)
![2023-08-13 08_29_26-.png](/assets/images/Projects/2023-08-13%2008_29_26-.png)
![2023-08-13 08_30_06-.png](/assets/images/Projects/2023-08-13%2008_30_06-.png)
![2023-08-13 08_30_35-.png](/assets/images/Projects/2023-08-13%2008_30_35-.png)
![2023-08-13 08_30_54-.png](/assets/images/Projects/2023-08-13%2008_30_54-.png)
8. Following the reboot, we should be presented with this screen. Proceed by inputting option `1`.
![2023-08-13 08_36_54-.png](/assets/images/Projects/2023-08-13%2008_36_54-.png)
9. Should VLANS be set up now[y:n]? `n` Enter em0, em1, em2, em3, em4, em5, in the order given for each subsequent question.
![2023-08-13 10_23_34-.png](/assets/images/Projects/2023-08-13%2010_23_34-.png)
10. Type `y` 
![2023-08-13 10_25_14-.png](/assets/images/Projects/2023-08-13%2010_25_14-.png)
11. Enter option `2` 
![2023-08-13 10_32_56-.png](/assets/images/Projects/2023-08-13%2010_32_56-.png)
12. Select the LAN Interface `2` 
![2023-08-13 10_35_50-.png](/assets/images/Projects/2023-08-13%2010_35_50-.png)
![2023-08-13 10_39_26-.png](/assets/images/Projects/2023-08-13%2010_39_26-.png)
![2023-08-13 10_40_32-.png](/assets/images/Projects/2023-08-13%2010_40_32-.png)
12. OPT1 Use the Configuration below set the IP `192.168.2.1` CIDR Notation `24`
![2023-08-13 10_45_31-.png](/assets/images/Projects/2023-08-13%2010_45_31-.png)
![2023-08-13 10_50_50-.png](/assets/images/Projects/2023-08-13%2010_50_50-.png)
![2023-08-13 10_52_06-.png](/assets/images/Projects/2023-08-13%2010_52_06-.png)
![2023-08-13 10_52_39-.png](/assets/images/Projects/2023-08-13%2010_52_39-.png)
13. OPT2 Use tje following configuration below use the IP `192.168.3.1` CIDR Notation `24`
![2023-08-13 10_56_38-.png](/assets/images/Projects/2023-08-13%2010_56_38-.png)
![2023-08-13 10_57_57-.png](/assets/images/Projects/2023-08-13%2010_57_57-.png)
14. Keep the OPT3 interface without an assigned IP address, as it will be utilized for the span port containing traffic monitored by Security Onion.
15. OPT4 use the following configuration below use IP `192.168.4.1` CIDR Notation `24`
![2023-08-13 11_02_37-.png](/assets/images/Projects/2023-08-13%2011_02_37-.png)
![2023-08-13 11_03_49-.png](/assets/images/Projects/2023-08-13%2011_03_49-.png)
16. It should look something like:
![2023-08-13 11_05_02-.png](/assets/images/Projects/2023-08-13%2011_05_02-.png)
This marks the completion of the PfSense VM configuration. Moving forward, the remaining configuration steps will be managed from the Kali machine, utilizing the WebConfigurator interface for the necessary adjustments and setups.