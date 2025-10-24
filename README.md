#  📘SIMATIC IPC227G – Full Setup & Configuration
This repo covers everything related to the Siemens Edge Device from installation and setup to complete deployment and usage (almost).

<p align="center">
  <img src="assets/image.png" width="400">
</p>


## 🧰Hardware Requirements

| Component | Minimum | Recommended |
|-----------|-----------|-----------|
| RAM (Memory) | 16 GB | 32 GB or higher |
| Hard Disk | 300 GB free | SSD preferred |
| CPU Cores | 4 | 8 |
| Network Interface | 1 (Bridged mode) | - |
| IP Configuration | Static IP required | - |

## 🖥️Software Requirements
- VMware Workstation Pro (Version 16 or later) [Link](https://www.vmware.com/products/desktop-hypervisor/workstation-and-fusion)
- Siemens Account [Link](https://www.siemens.com/global/en.html)
- Industrial Edge Management (IEM) Hub Access

## ⚙️Pre-Configuration Steps
1) Create/Register a Siemens Account
2) Verify via Email and Login
3) Access the IEM Hub to manage user panels and instances.

## 🛠️Configuration Steps
### 1️⃣ Launch VMware Workstation Pro
- Ensure VMware is properly installed and licensed.
- Verify all network adapters are active.

### 2️⃣ Import Virtual Machine
- Go to File → Open (Ctrl + O).
- Select the downloaded .ova file and Import it.
- Assign a name and choose a suitable storage location.

### 3️⃣ Configure Network in VMware
- Go to Edit → Virtual Network Editor.
- Click Change Settings.
- Under VMnet0, set Network Type → Bridged.
- Select your physical network adapter and apply changes.

  | ⚠️ _Bridged mode allows the VM to act as a separate device on the same network as the host._

### 4️⃣ Power On the Virtual Machine
- Click Power on this Virtual Machine.
- Wait for the IEM to boot.
- Note the IP address displayed on the screen.

### 5️⃣ Access Configuration Portal
- Open a browser and enter the displayed IP.
- The IEM setup interface will appear.

## 🌐Network Configuration

| Parameter | Value |
|-----------|-----------|
| IP Address | `192.168.1.140` |
| Subnet Mask | `255.255.255.0` | 
| Gateway | `192.168.1.1` |
| Primary DNS | `8.8.8.8` |
| Secondary DNS | `1.1.1.1` |

Click `Update`, wait for the system to apply changes, and refresh the page with the new IP.

## 🔑User Credentials
- Set up your username and password.
- Click `Next` to continue.

## 📦Provisioning File Upload

1) In IEM Hub, go to Instances → Create New Instance.
2) Enter an instance name and download the provisioning file (.zip / .json).
3) Upload the file in the configuration screen.
4) Click `Next` to proceed.

## 🌍Configure FQDN
_This is an optional step, feel free to skip this_
- Add a custom domain (e.g., iem.localdomain).
- Click `Next`.

## 🧾Recovery Key & Submission

- Note down the generated Recovery Key.
- Click Submit to finalize setup.
- Wait a few minutes for automatic configuration.

## ✅Verify Setup
- Go to IEM Hub ➡️ Instances.
- Check if the instance status is Active.
- If it’s still Pending, refresh after a few minutes.

## 📂Access Edge Management Dashboard
- Click Edge Management.
- Login with your credentials.
- You’ll be directed to the IEM Home Screen.
