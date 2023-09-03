---
title: Installing Kali Linux and Setting up Pfsense
author: Arsenio Brown 
date: 2023-09-02 12:00:00 +0000  # Replace with today's date and time
categories: [Cybersecurity, Labs, Kali]
tags: [Threat Hunting, Network Security, Malware]
image:
  path: /assets/images/Kali/hacker-8198734_1280.jpg
  alt: Installing Kali and Setting up Pfsense
---
## Installing and Setting up Kali 
Download Kail Linux ISO [Kali Linux](https://www.kali.org/get-kali/#kali-virtual-machines)

We Will be Downloading the VMware iso for Kali. 

![Pasted image 20230902000853.png](/assets/images/Kali/Pasted image 20230902000853.png)

After Downloading extract the file locate the vmx file and double click. This should launch you into vmware.

![Pasted image 20230902001710.png](/assets/images/Kali/Pasted image 20230902001710.png)

After the app opens we just want to make a couple changes. click on `Edit virtual machine settings`

![[2023-09-02 00_19_08-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png]](/assets/images/Kali/2023-09-02 00_19_08-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png)

click `add` to add a new Network Adaptor

![2023-09-02 00_22_03-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png](/assets/images/Kali/2023-09-02 00_22_03-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png)
change Network adaptor2 to Vmnet2 then click on.
![[2023-09-02 00_23_36-Virtual Machine Settings.png]](/assets/images/Kali/2023-09-02 00_23_36-Virtual Machine Settings.png)
Power on the machine
![[2023-09-02 00_25_29-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png]](/assets/images/Kali/2023-09-02 00_25_29-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png)
Username = `kali`
Password = `kali`
We need to change that to do so press `ctrl and ALT and t` to open a terminal and type `passwd` and follow the prompt
![[2023-09-02 00_27_58-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png]](/assets/images/Kali/2023-09-02 00_27_58-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png)
![[2023-09-02 00_32_48-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png]](/assets/images/Kali/2023-09-02 00_32_48-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png)

## Setting up Pfsense 
Open Firefox and type `192.168.1.1` 
![[2023-09-02 00_37_54-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png]](/assets/images/Kali/2023-09-02 00_37_54-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png)
Username = `admin`

Password = `pfsense`
![[2023-09-02 00_40_01-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png]](/assets/images/Kali/2023-09-02 00_40_01-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png)
![[2023-09-02 00_42_07-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png]](/assets/images/Kali/2023-09-02 00_42_07-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png)
For DNS type `8.8.8.8` and `8.8.4.4`

Chose your TZ
![[2023-09-02 00_43_36-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png]](/assets/images/Kali/2023-09-02 00_43_36-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png)
Uncheck these settings
![[2023-09-02 00_45_49-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png]](/assets/images/Kali/2023-09-02 00_45_49-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png)
![[2023-09-02 00_47_55-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png]](/assets/images/Kali/2023-09-02 00_47_55-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png) Change Lan to Kali

![[2023-09-02 00_53_01-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png]](/assets/images/Kali/2023-09-02 00_53_01-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png)
![[2023-09-02 00_54_30-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png]](/assets/images/Kali/2023-09-02 00_54_30-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png)
OPT1 change to `VICTIMNETWORK`
![[2023-09-02 00_57_45-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png]](/assets/images/Kali/2023-09-02 00_57_45-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png)
OPT2 change `SecOnion`
OPT3 change to `SpanPort` Be sure to click enable interface
![[2023-09-02 01_04_04-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png]](/assets/images/Kali/2023-09-02 01_04_04-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png)

Go to Bridges and click add and for Member Interfaces select Victimnetwork and click display Advanced select span port and chose SPANPORT then Save
![[2023-09-02 01_08_09-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png]](/assets/images/Kali/2023-09-02 01_08_09-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png)
![[2023-09-02 01_09_13-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png]](/assets/images/Kali/2023-09-02 01_09_13-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png)
![[2023-09-02 01_10_11-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png]](/assets/images/Kali/2023-09-02 01_10_11-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png)
![[2023-09-02 01_11_32-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png]](/assets/images/Kali/2023-09-02 01_11_32-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png)
![[2023-09-02 01_12_26-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png]](/assets/images/Kali/2023-09-02 01_12_26-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png)

OPT4 change to `Splunk` Also ensure you Apply the changes.
![[2023-09-02 01_01_29-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png]](/assets/images/Kali/2023-09-02 01_01_29-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png)
Now We need to setup firewall rules
![[2023-09-02 01_14_16-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png]](/assets/images/Kali/2023-09-02 01_14_16-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png)

![[2023-09-02 01_23_47-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png]](/assets/images/Kali/2023-09-02 01_23_47-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png)

![[2023-09-02 01_26_59-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png]](/assets/images/Kali/2023-09-02 01_26_59-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png)
![[2023-09-02 01_28_05-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png]](/assets/images/Kali/2023-09-02 01_28_05-kali-linux-2023.3-vmware-amd64 - VMware Workstation.png)
