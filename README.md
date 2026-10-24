<h1 align="center">🎮 PS4 / PS4 Pro (Belize) Initramfs Patch (ext4) 🚀</h1>
<p align="center"><b>Simple Guide to Run Linux</b></p>


> [!TIP]
> **100% Stable.** Built on `better_initramfs_v0.9.1`. Designed exclusively for PS4 / PS4 Pro (Belize Southbridge).
> 
> 💬 **If you have any questions or face any issues, feel free to send me a message or open an issue here on GitHub!**

### 🛑 Stop the Reinstall Loop!
Are you tired of the `"Structure needs cleaning"` error? Or maybe you just want to start fresh without worrying about future crashes? 

**Even if you don't have problems right now, I highly recommend building your system from scratch using `ext4`.** It completely replaces the old, fragile file system, giving you peace of mind and saving you from future headaches.

Switching from `ext2` to **`ext4`** fixes this permanently:
*   🚀 **Better Performance:** Faster and smoother read/write speeds.
*   🛡️ **Crash Protection (Journaling):** If your PS4 crashes or loses power, `ext4` automatically repairs itself on the next boot. No more corrupted data.

---

### 💿 Recommended Distro: CachyOS Light LXQt
You **MUST** use a distro built specifically for the PS4. You can find most of them on [ps4linux.com](https://ps4linux.com/). 

I highly recommend using **CachyOS Light LXQt** from this thread: 
👉 [CachyOS Light LXQt - A light and fast distro](https://ps4linux.com/forums/d/422-cachyos-light-lxqt-a-light-and-fast-distro)

**Why is it good?**
*   **Light & Fast:** It's bare bones, simple, and doesn't get in your way.
*   **PS4-Specific Mesa:** It includes PS4-specific **Mesa 26.0.4 (GPU) drivers** out of the box, updated automatically with Pacman for the best GPU performance.
*   **Ready to Use:** Comes with uBlock Origin, BetterFox pre-installed, and a Picom compositor (disabled by default for max performance).

*Note: The system file can be `psxitarch.tar.xz` or `psxitarch.tar.gz`.*

---

### 📂 Where to Put the Files:
Use FTP (explained below) to transfer the files.

1.  **Kernel & Initramfs:**
    *   Path: **`/user/data/linux/boot/`**
    *   Put: `bzImage`, `bootargs.txt`, `initramfs.cpio`.
    *   *Note: Create the `linux/boot` folders manually if they don't exist.*
2.  **Linux System (Distro Archive):**
    *   Path: **`/user/system/boot/`**
    *   Put: `psxitarch.tar.xz` (or `.tar.gz`).

---

### 📡 File Transfer (FTP):
*Your PC/Phone and PS4 must be on the same Wi-Fi.*

1.  Go to **GoldHEN Settings** -> Turn on **FTP Server** and **Payload Server**. Note the IP address.
2.  **PC:** Use **FileZilla**. Enter IP, Port **`2121`**, click Quickconnect.
3.  **Phone:** Use **AndFTP**. Enter IP, Port **`2121`**. 
    *(Tip: Tap the phone icon at the top to switch between your phone storage and PS4 files).*

---

### 🛠️ Installation Steps:
> [!IMPORTANT]
> **Prerequisites:** PS4 Firmware **13.52 or lower**. 

1.  **Exploit (Internet ON):** Open PS4 browser -> `https://webkitty.arabpixel.net/` -> Run GoldHEN.
2.  **Internet OFF:** Once GoldHEN is loaded, turn off PS4 internet.
3.  **Run Payload:** GoldHEN -> Utilities -> **Payloader** -> Select your payload. (It is recommended to use **1GB VRAM** just for the installation process).
4.  **Install:** In the Linux terminal, type:
    ```bash
    install-linux-hdd.sh
    ```
5.  **Allocate Space & Wait:** Enter your desired size (e.g., `300`) and press Enter. 
    > [!NOTE]
    > **Wait Time:** The installation process might take **5 to 20 minutes** to complete. Please let it finish.

---

### 🎮 VRAM Allocation (After Installation):
Once the installation is complete, you can change your payload to allocate more VRAM depending on what you plan to do:
*   **2GB VRAM:** Best for web browsing and light games.
*   **3GB VRAM:** Use this if you plan to play heavier games.
*   **⚠️ DO NOT use 4GB VRAM.** It causes severe instability and crashes.

---

### 💾 How to Prepare the Payload:
1. Download payload from [ps4-linux-loader](https://github.com/ps4-linux/ps4-linux-loader/releases).
2. Extract the `.zip`, go to `elf` folder, pick your desired VRAM size.
3. Rename the file from `.elf` to `.bin`.
4. Put it on a **FAT32 USB drive**.
    *   *PC:* Use GParted (Linux) or Windows Format.
    *   *Android:* Use an OTG cable and the **USB Master** app to format to FAT32 and copy the file.

---

> [!CAUTION]
> **WARNINGS:**
> *   💾 **SPACE LIMIT:** Don't enter a GB size larger than your actual free space.

---
> [!NOTE]
> **This is NOT AI slop.** This is a real, tested patch made by a human to save you from file corruption headaches.
