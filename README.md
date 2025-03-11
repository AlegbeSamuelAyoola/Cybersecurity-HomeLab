# Cybersecurity Home Lab Documentation (Part 1 of 3)

This repository documents my journey setting up a cybersecurity home lab using **Windows 10 Tiny** and **Kali Linux** on **VMware**, running on my **ThinkPad X260** with **8GB RAM** and a **256GB SSD**. This is Part 1 of a 3-part series, and I'll be updating it with more advanced configurations in later parts.

## Table of Contents

- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Setup Instructions](#setup-instructions)
  - [Installing VMware Workstation Player](#installing-vmware-workstation-player)
  - [Setting Up the Virtual Machines](#setting-up-the-virtual-machines)
    - [Windows 10 Tiny VM](#windows-10-tiny-vm)
    - [Kali Linux VM](#kali-linux-vm)
  - [Optimizing VMware Settings](#optimizing-vmware-settings)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Overview

This project demonstrates how to build a lightweight cybersecurity home lab using consumer-grade hardware. The focus is on achieving smooth performance with limited resources by using a stripped-down version of Windows (Windows 10 Tiny) and Kali Linux as a penetration testing platform—all virtualized with VMware Workstation Player.



<div class="container">
  <div class="text">Lab Setup Overview</div>
  <img src="Images/lab-setup-diagram.png" alt="Lab Setup Diagram" width="600">
</div>


## Prerequisites

Before starting, ensure you have:
- **Hardware:** ThinkPad X260 with 8GB RAM and 256GB SSD, Intel Core i5 Processor, or equivalent.
- **Software:** 
  - [VMware Workstation Player](https://www.vmware.com/products/workstation-player.html)
  - Windows 10 Tiny ([Host OS image or VM file](https://archive.org/details/tiny11-2311))
  - Kali Linux VM file (download from the [official Kali website](https://www.kali.org/get-kali/))

## Setup Instructions

### Installing VMware Workstation Player
1. Download and install VMware Workstation Player from the official website.
2. Follow the on-screen instructions and reboot your system after installation.



<div class="image-container">
  <div class="text"><strong>VMware Installation</strong></div>
  <img src="Images/vmware-installation.png" alt="VMware Installation" width="600">
</div>


### Setting Up the Virtual Machines

#### Windows 10 Tiny VM
1. Open VMware and click **Open a Virtual Machine**.
2. Select your Windows 10 Tiny VM file.
3. **Allocate 3GB of RAM** to Windows 10 Tiny. *(I was surprised at how smoothly it ran with this limited allocation.)*
4. Configure storage and network settings as needed.

<details>
  <summary>📷 Windows 10 Tiny Installation Steps (Click to Expand)</summary>

   ## Windows VM Settings



 <div class="container">
  <div class="text">Open the VMware Workstation Player and create a new virtual machine</div>
  <img src="Images/windows-vm-settings2.png" alt="Create a new VM" width="600">
 </div>

 <div class="container">
  <div class="text">Navigate to the Windows 10 Tiny ISO file and select it</div>
  <img src="Images/windows-vm-settings3.png" alt="Select Windows 10 Tiny ISO" width="600">
 </div>

 <div class="container">
  <div class="text">Input a name for the virtual machine</div>
  <img src="Images/windows-vm-settings4.png" alt="Input a VM name" width="600">
 </div>

 <div class="container">
  <div class="text">Make sure the network adapter is set to NAT (Network Address Translation) and click OK</div>
  <img src="Images/windows-vm-settings5.png" alt="Set network adapter to NAT" width="600">
 </div>

 <div class="container">
  <div class="text">Click on finish to save</div>
  <img src="Images/windows-vm-settings6.png" alt="Finish VM setup" width="600">
 </div>

 <div class="container">
  <div class="text">It will take some time to create the virtual machine</div>
  <img src="Images/windows-vm-settings7.png" alt="VM creation progress" width="600">
 </div>

 <div class="container">
  <div class="text">Start the virtual machine</div>
  <img src="Images/windows-vm-settings7.1.png" alt="Start VM" width="600">
 </div>

 <div class="container">
  <div class="text">The machine will boot up</div>
  <img src="Images/windows-vm-settings8.png" alt="VM booting up" width="600">
 </div>

 <div class="container">
  <div class="text">Make your selections and click on next</div>
  <img src="Images/windows-vm-settings9.png" alt="Make selections and continue" width="600">
 </div>

 <div class="container">
  <div class="text">Windows will install</div>
  <img src="Images/windows-vm-settings10.png" alt="Windows installation in progress" width="600">
 </div>

 <div class="container">
  <div class="text">Select your region</div>
  <img src="Images/windows-vm-settings11.png" alt="Select region" width="600">
 </div>

 <div class="container">
  <div class="text">Create a username & password</div>
  <img src="Images/windows-vm-settings12.png" alt="Create user credentials" width="600">
 </div>

 <div class="container">
  <div class="text">Create a username & password</div>
  <img src="Images/windows-vm-settings13.png" alt="Create user credentials" width="600">
 </div>

 <div class="container">
  <div class="text">Disable unnecessary settings</div>
  <img src="Images/windows-vm-settings14.png" alt="Disable unnecessary settings" width="600">
 </div>

 <div class="container">
  <div class="text">Windows will take a few minutes to boot, take a break!</div>
  <img src="Images/windows-vm-settings15.png" alt="Windows booting up, take a break" width="600">
 </div>

 <div class="container">
  <div class="text">Windows has successfully booted!</div>
  <img src="Images/windows-vm-settings16.png" alt="Windows booted successfully" width="600">
 </div>

 </details>

#### Kali Linux VM
1. Open the Kali Linux VM file in VMware.
2. **Allocate 4GB of RAM** and **2 processor cores** to Kali Linux.
3. Finish setting up by adjusting storage and network settings.

<details>
  <summary>📷 Kali Linux Installation Steps (Click to Expand)</summary>



 <div class="container">
  <div class="text">Search for Kali Linux</div>
  <img src="Images/kali-vm-settings1.png" alt="Search for Kali Linux" width="600">
 </div>

 <div class="container">
  <div class="text">Enter the Kali website</div>
  <img src="Images/kali-vm-settings2.png" alt="Enter the Kali website" width="600">
 </div>

 <div class="container">
  <div class="text">Navigate to the VMware image file</div>
  <img src="Images/kali-vm-settings3.png" alt="Navigate to the VMware image file" width="600">
 </div>

 <div class="container">
  <div class="text">
    Download 7-zip (<a href="https://www.7-zip.org/download.html" target="_blank" style="color: yellow;">7-zip</a>)
  </div>
 </div>

 <div class="container">
  <div class="text">Extract the VM file downloaded from Kali Linux</div>
  <img src="Images/kali-vm-settings4.png" alt="Extract the VM file" width="600">
 </div>

 <div class="container">
  <div class="text">Navigate to the extracted folder</div>
  <img src="Images/kali-vm-settings5.png" alt="Navigate to extracted folder" width="600">
 </div>

 <div class="container">
  <div class="text">Make sure a file with the extension (.vmx) is present</div>
  <img src="Images/kali-vm-settings6.png" alt="Check for .vmx file" width="600">
 </div>

 <div class="container">
  <div class="text">Open the VMware Workstation Player</div>
  <img src="Images/kali-vm-settings7.png" alt="Open VMware Workstation Player" width="600">
 </div>

 <div class="container">
  <div class="text">Create a new virtual machine, then navigate to the .vmx file and select it</div>
  <img src="Images/kali-vm-settings8.png" alt="Select .vmx file" width="600">
 </div>

 <div class="container">
  <div class="text">Navigate to the virtual machine settings and increase the RAM to 4GB</div>
  <img src="Images/kali-vm-settings9.png" alt="Increase RAM to 4GB" width="600">
 </div>

 <div class="container">
  <div class="text">Start the virtual machine & select the first option</div>
  <img src="Images/kali-vm-settings10.png" alt="Start Kali VM" width="600">
 </div>

 <div class="container">
  <div class="text">Default username & password is kali/kali</div>
  <img src="Images/kali-vm-settings11.png" alt="Login credentials" width="600">
 </div>

 <div class="container">
  <div class="text">You are logged in!</div>
  <img src="Images/kali-vm-settings12.png" alt="Logged into Kali Linux" width="600">
 </div>


 </details>

### Optimizing VMware for Performance
- **Enable VT-x/AMD-V in BIOS:** Ensure virtualization is enabled.
- **Resource Allocation:** Fine-tune RAM and CPU settings between host and guest OS.
- **Network Settings:**  
  - **NAT:** Provides security by hiding the VM behind the host’s IP. *(Recommended for isolation.)*  
  - **Bridged Networking:** Use if the VM needs its own IP for direct communication.  

## Future Enhancements

✅ **Future Documentation Updates:**
- [ ] 🔜 Part 2: [SIEM Integration](./SIEM%20Integration.md)
- [ ] 🔜 Part 3: Automating SOC Processes with Python & Bash (Coming Soon!)

## Contributing

Contributions are welcome! If you have improvements or additional insights, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For questions or suggestions, please open an issue or contact me via GitHub or on my X page.

Happy hacking—and have fun learning!
