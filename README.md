# MOIC - macOS Icon Changer

A lightweight bash script to customize system application icons and the Finder Dock icon on modern macOS versions (Big Sur and later).

## ⚠️ Warning

This script modifies the Signed System Volume (SSV). By committing these changes, you will create a new system snapshot. **Use at your own risk and always keep backups of your original icon files.**

## Prerequisites

To allow the script to mount the system volume for writing, you must disable **SIP** and **Authenticated Root** from Recovery Mode:

1. Reboot into **Recovery Mode** (Hold Cmd+R or Power button).
2. Open **Terminal**.
3. Run the following commands:
```bash
csrutil disable
csrutil authenticated-root disable

```


4. Reboot back to macOS.

## Usage

1. Clone the repository:
```bash
git clone https://github.com/ConradZn/macOS-Icon-Changer.git
cd macOS-Icon-Changer

```


2. Make the script executable:
```bash
chmod +x IconChanger.sh

```


3. Run with root privileges:
```bash
sudo ./IconChanger.sh

```



## Features

* **System Apps:** Easily open the protected `/System/Applications` folder to swap icons.
* **Finder Icon:** Replace the hardcoded Dock Finder icon.
* **Automated Snapshot:** Handles the `bless` command and snapshot creation to make changes persistent.
* **Cache Cleaning:** Automatically flushes icon services and Dock caches to ensure new icons appear immediately.

## Credits

* **Author:** [ConradZn](https://github.com/ConradZn)
* **Original Logic:** Based on Big Sur Icon Changer by HueZuX
