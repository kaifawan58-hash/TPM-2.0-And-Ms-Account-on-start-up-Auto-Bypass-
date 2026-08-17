# Windows 11 Unattended Installer — Hardware Bypass

A pre-configured `autounattend.xml` for automating a clean Windows 11 installation while attempting to bypass common hardware compatibility checks and reduce setup prompts.

> ⚠️ **Warning:** This project can automate disk and partition operations. **Back up all important data before installing Windows.** Carefully verify the target drive before proceeding.

## Features

* **Hardware compatibility bypass** — Attempts to skip Windows 11 checks for:

  * TPM 2.0
  * Secure Boot
  * Unsupported CPUs
  * RAM requirements
  * Storage requirements
* **Local account setup** — Avoids requiring a Microsoft account where supported.
* **Offline-friendly installation** — Designed to minimize dependency on an internet connection during setup.
* **Automated setup** — Reduces manual interaction with Windows Setup.
* **EULA and setup automation** — Automatically handles supported setup prompts and configuration steps.

> **Compatibility note:** Microsoft may change Windows Setup behavior between releases. Bypass mechanisms that work with one Windows 11 version may not work with another.

## Requirements

* A Windows 11 ISO
* A USB flash drive suitable for Windows installation
* A tool for creating bootable Windows media, such as Rufus
* The included `autounattend.xml`
* A computer capable of booting from USB

## Installation

### 1. Download the Repository

Clone or download this repository and locate:

```text
autounattend.xml
```

### 2. Create Windows 11 Installation Media

Create a bootable USB drive from your Windows 11 ISO using your preferred tool.

### 3. Copy the Answer File

Copy `autounattend.xml` to the **root of the USB drive**, alongside the Windows Setup files:

```text
USB Drive/
├── autounattend.xml
├── boot/
├── efi/
├── sources/
├── support/
└── setup.exe
```

### 4. Boot from the USB

Insert the USB drive into the target PC and boot from it.

Windows Setup should automatically detect the answer file and apply the configured installation settings.

### 5. Verify the Target Disk

If the configuration includes automated partitioning or disk operations, **make absolutely sure the correct drive is selected** before proceeding.

## Customization

The answer file can be customized to suit different deployment scenarios.

Possible customizations include:

* Local user accounts
* Computer name
* Regional and language settings
* Automated partition layouts
* Windows edition selection
* Setup preferences
* First-logon commands
* Registry configuration
* Optional post-installation tasks


**Free To Use**
