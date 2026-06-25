
# Upgrade to ProjectBlaze 🚀

An automated, user-friendly Android flashing utility designed seamlessly for the BlazeOS desktop ecosystem. This tool bridges the gap between your desktop and mobile experience, allowing users to transition their supported Android devices directly to **ProjectBlaze ROM** with just a few clicks.

Built using **Python**, **PyQt6**, and a robust modular background engine, it handles device detection, recovery image sourcing, safe downloading, and automated execution of `adb` and `fastboot` routines.
<img width="1173" height="809" alt="resim(3)" src="https://github.com/user-attachments/assets/708dee42-71c9-4eb6-a484-cf8e05246c18" />

---

## ✨ Features

* **⚡ Automated Device Detection:** Real-time monitoring and identification of connected Android devices via ADB/Fastboot.
* **🌐 Smart Recovery Finder:** Automatically fetches the compatible custom recovery image (TWRP, OrangeFox, etc.) tailored for your specific device codename.
* **📥 Async Multi-threaded Downloader:** Downloads ROM and recovery assets smoothly without freezing the sleek modern UI.
* **🔒 Fail-Safe Flashing Engine:** Sequences flashing protocols securely—rebooting to bootloader, flashing recovery, entering `fastbootd`, wiping, and sideloading the ProjectBlaze ROM.
* **🎨 Material-Inspired UI:** Features a native, clean, and intuitive layout built on top of the BlazeOS design philosophy.
<img width="1175" height="802" alt="resim(2)" src="https://github.com/user-attachments/assets/fff825d5-89bf-43ab-b04c-89ff8529edbb" />


---

## 🏗️ Architecture

The tool is split into highly independent, reusable modules to ensure reliability:

* **`blazeflash.py`**: The main entry point initializing the application lifecycle.
* **`main_window.py`**: The responsive core GUI interface built with PyQt6.
* **`device_detector.py`**: Continuously checks connection states and toggles between ADB and Fastboot tracking.
* **`recovery_finder.py`**: Resolves device codenames to matching recovery image URLs.
* **`downloader.py`**: Handles background networking operations safely using `QThread`.
* **`flash_engine.py`**: Wraps native system calls to execute precision partitioning and flashing commands.
<img width="1173" height="808" alt="resim(4)" src="https://github.com/user-attachments/assets/106ed265-3027-47a1-9f27-6b01c7052b5d" />

---

## 🛠️ Requirements & Installation

This utility comes pre-installed out of the box on upcoming **BlazeOS Fedora & Debian** releases. If you are setting up a development environment manually:

### Prerequisites
Make sure your system has `android-tools` (containing `adb` and `fastboot`) installed and configured in your PATH environment variable.
