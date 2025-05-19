# Manjaro VR Installer - Read Me

Welcome to your all-in-one VR setup for Manjaro Linux. This script helps get your system fully VR-ready with tools like Unity Hub, ALVR, and WiVRn while keeping everything as native as possible.

---

## 📦 What This Installs

This script installs the following tools and services:

* **Unity Hub (Flatpak)** – Required for VRChat world/avatar development
* **Unity 2022.3.22f1** – The version needed for VRChat (manual install)
* **ALCOM** – VRChat-compatible project launcher and toolkit
* **ALVR (AUR)** – Wireless PC VR streaming over Wi-Fi
* **WiVRn (Flatpak)** – Alternative VR streaming tool
* **Discord (Snap)** – Communication platform for devs and VRChat communities
* **Blender** – 3D modeling
* **GIMP** – Image editing
* **Audio/VR tools** – `pavucontrol`, `pipewire`, `helvum`, etc.
* **Developer utilities** – `xdotool`, `wmctrl`, `jq`, `git`, etc.
* **Avahi/mDNS** – For device discovery in VR setups

---

## 📁 Installation Instructions

### 1. **Unpack and Move**

* Unzip the downloaded archive.
* Move the entire `Program Files` folder into your **Home** directory (`/home/yourname`).

### 2. **Run the Installer**

* Double-click `linux-vr-setup`.
* If it doesn't run, do this:

  * Right-click `linux-vr-setup` > **Properties** > **Permissions tab**.
  * Check the box: `Allow executing file as program`.
  * Then double-click it again.

### 3. **Enter Your Password**

* You will be prompted for your password (due to `sudo`).
* Just type it and press **Enter** — you won’t see the characters as you type.
* You may need to enter your password **multiple times**.

### 4. **Snap Discord Install**

* When Discord is being installed via Snap, it may **require a reboot**.

### 5. **Post-Reboot**

* After rebooting, run `linux-vr-setup` again.
* Enter your password again if prompted.
* Your browser will open automatically.

### 6. **Download and Place ALCOM**

* Download **ALCOM Linux** from the link that opens.
* Move the AppImage into `~/Program Files`.
* Open a terminal and run:

  ```bash
  yay -S vrc-get
  ```
* Enter password if asked.

---

## 🎮 Unity Hub & VRChat Creator Instructions

Unity 2022 is currently broken and will not allow login with some installs. To work around this:

1. Run the **launcher** to open Unity Hub (installed via Flatpak).
2. Log in to Unity Hub.
3. Go to [Unity Archive](https://unity.com/releases/editor/archive) and manually install:

   * `Unity 2022.3.22f1`
4. Once installed, **close the launcher**.
5. Run the launcher **again**.
6. In ALCOM's **Settings**, add the Unity install path:

   ```
   /home/yourname/Program Files/unity/hub/editor/2022.3.22f1/editor
   ```
7. If it asks for an executable, choose the file named `Unity` inside the above folder.
8. You should now be good to go!

> ✅ **Tip:** Occasionally open the launcher to keep Unity login tokens up to date.

---

## ☕ Support & Notes

* Unity Hub is a **Flatpak** due to login issues in native/other versions.
* All other tools install **natively** or via AUR where possible.
* Snap is only used where **absolutely necessary** (Discord).

You're now VR-ready on Manjaro. Happy creating! 🚀
