# TPM-2.0-And-Ms-Account-on-start-up-Auto-Bypass-
AutoMatically Bypass TPM 2.0 OR MS Account On Start up 
# Windows 11 Automated & Unattended Setup

This repository provides a pre-configured `autounattend.xml` answer file designed to streamline and automate the clean installation of Windows 11. By utilizing the official Microsoft Windows Deployment framework, this file automatically injects required configuration tweaks and skips restrictive setup phases right at boot.

## 🌟 Key Features

* **Hardware Restriction Bypass:** Automatically bypasses Windows 11 installation requirements for **TPM 2.0, Secure Boot, RAM size, Storage space, and CPU generation** during the initial setup phase.
* **Account Requirement Bypass:** Bypasses the forced internet connection requirement (`BypassNRO`) and completely skips the mandatory "Sign in with a Microsoft Account" screen.
* **Streamlined Experience:** Hides unnecessary setup screens including the EULA, OEM registration, and privacy configurations for a faster deployment.

This is an ideal administrative tool for IT professionals, developers, and enthusiasts looking to deploy Windows 11 on older hardware, virtual machines (VMs), or test environments without manual intervention.

---

## 🚀 How to Use This File

### Step 1: Create a Windows 11 Installation USB
1. Plug a blank USB flash drive (at least 8GB) into your computer.
2. Download the official **Windows 11 Media Creation Tool** from Microsoft.
3. Run the tool and follow the prompts to create a bootable Windows 11 USB flash drive.

### Step 2: Download and Copy the XML File
1. Download the `autounattend.xml` file from this repository.
2. Copy the `autounattend.xml` file.
3. Open your Windows 11 USB drive and paste the file directly into the **root directory** (the main folder of the USB, right next to the `setup.exe` file). 

> ⚠️ **Important:** Do *not* put it inside the `sources` folder or any sub-folders. It must sit on the main screen of the USB drive.

### Step 3: Boot and Install
1. Plug the USB drive into the target computer.
2. Turn on the PC and instantly tap your computer's boot menu key (usually `F12`, `F11`, `F8`, or `Esc`) to select the USB drive.
3. The Windows installer will launch and read your `autounattend.xml` file. It will automatically bypass all hardware checks and skip the Microsoft Account login screen without you needing to click anything.
