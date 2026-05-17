# MOIC - macOS Icon Changer

A lightweight bash script to customize system application icons and the Finder Dock icon on modern macOS versions (Big Sur and later).

---

## ⚠️ Warning

This script modifies the Signed System Volume (SSV). By committing these changes, you will create a new system snapshot. **Use at your own risk and always keep backups of your original icon files.**

---

## Prerequisites

To allow the script to mount the system volume for writing, you must disable **SIP** and **Authenticated Root** from Recovery Mode:

1. Reboot into **Recovery Mode** (Hold `Cmd+R` on Intel or hold the `Power button` on Apple Silicon).
2. Open **Terminal** from the Utilities menu.
3. Run the following commands:

```bash
csrutil disable

```

```bash
csrutil authenticated-root disable

```

4. Reboot back to macOS.

---

## Usage

1. Clone the repository:

```bash
git clone https://github.com/ConradZn/macOS-Icon-Changer.git

```

```bash
cd macOS-Icon-Changer

```

2. Run via Terminal:

```bash
sh ./IconChanger_ConradZn.sh

```

---

## How to Change the Icons (Step-by-Step)

Once you run the script, the writable `/System/Applications` folder will open automatically. Follow these steps to manually swap the icons:

1. **Open Second Finder Windows:**
Keep the automatically opened `/System/Applications` window on one side of your screen. Open a second Finder window next to it with your downloaded **macOS Tahoe Icons** (.icns files).
2. **Open App Info:**
In the System Applications folder, right-click (or `Ctrl + Click`) the app you want to customize and select **Get Info**. A small properties window will pop up.
3. **Drag and Drop:**
Drag the new `.icns` file from your Tahoe Icons folder and drop it **directly onto the small app icon** located at the very top-left corner of the "Get Info" window.
4. **Enter Password:**
macOS will prompt you for your administrator password to confirm the change on the system volume. Type your password and hit Enter.

---

## Features

* **System Apps:** Easily open the protected `/System/Applications` folder to swap icons.
* **Finder Icon:** Replace the hardcoded Dock Finder icon.
* **Automated Snapshot:** Handles the `bless` command and snapshot creation to make changes persistent.
* **Cache Cleaning:** Automatically flushes icon services and Dock caches to ensure new icons appear immediately.

---

## Credits

* **Author:** [ConradZn](https://github.com/ConradZn)
* **Original Logic:** Based on Big Sur Icon Changer by HueZuX
* **Featured Icons:** Includes the gorgeous **macOS Tahoe Icons** collection. You can preview and download the full icon pack directly from this [Google Drive Folder](https://drive.google.com/drive/folders/1YZvlCIGjUntSpM-6g2yrYvctOBPcvlNg?usp=share_link).
