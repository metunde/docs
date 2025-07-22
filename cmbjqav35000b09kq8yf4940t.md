---
title: "Forgotten Password? Don't Wipe Your Linux Machine!"
datePublished: Thu Jun 05 2025 18:47:30 GMT+0000 (Coordinated Universal Time)
cuid: cmbjqav35000b09kq8yf4940t
slug: forgotten-password-dont-wipe-your-linux-machine
tags: linux, cli, devops, passwords

---

**🔐 How to Reset a Linux Machine Password (Linux Mint) Using a Live USB**

I forgot my machine’s password a few weeks ago, even though it was a practice environment with no essential resources on it, and I could have easily just reloaded the OS. But I decided to challenge myself and find a way to get back in - and I did. I also decided to document the process for any curious person or anyone who may need this.

---

**✅ What You’ll Need**

* A bootable **USB or DVD** (same version as your installed system).
    
* A basic understanding of using the terminal.
    

---

**🖥️ Step-by-Step Guide**

**🔹 Step 1: Boot Into the Live Session**

1. Insert the Linux Mint Live USB or DVD into your computer while it’s still switched off.
    
2. Switch on the machine and press the boot options key ( press F9 on hp)-I usually press repeatedly immediately the machine is on.
    
3. Select **"Try Linux Mint"** at the boot menu to enter the live environment.
    

---

**🔹 Step 2: Open the Terminal**

Once the desktop loads, open the terminal at the bottom panel or press **Ctrl + Alt + T** to open a terminal window.

---

**🔹 Step 3: Identify Your Root Partition**

Run the following command to list all partitions:

sudo fdisk -l

Look for your Linux system’s root partition. It will usually be something like /dev/sda2 and have a Linux filesystem as the type.

---

**🔹 Step 4: Mount the Root Partition**

Replace /dev/sda2 with your actual root partition with:

sudo mount /dev/sda2 /mnt

If /boot is on a separate partition (e.g., /dev/sda1), mount that as well with:

sudo mount /dev/sda1 /mnt/boot

---

**🔹 Step 5: Bind System Directories**

These commands prepare the chroot environment:

sudo mount --bind /dev /mnt/dev

sudo mount --bind /proc /mnt/proc

sudo mount --bind /sys /mnt/sys

---

**🔹 Step 6: Chroot Into Your Installed System**

Run:

sudo chroot /mnt

Now you’re operating **inside your installed system**, as if you had booted normally.

---

**🔹 Step 7: Reset the User Password**

Now reset the password. Replace your-username with your actual username:

passwd your-username

Enter the new password twice when prompted.

Don’t know your username? You can check with:

ls /home

---

**🔹 Step 8: Exit and Reboot**

Exit the chroot environment and unmount the partitions:

exit

sudo umount /mnt/dev

sudo umount /mnt/proc

sudo umount /mnt/sys

sudo umount /mnt

sudo reboot

---

**✅ You're Done!**

After rebooting, remove the Live USB/DVD. Your system should boot normally, and you can log in with your **new password**.

---

**✅ Distributions Where This Works**

The method works reliably on:

* **Ubuntu** and all its derivatives
    
* **Debian**
    
* **Arch Linux** and all of its derivatives.
    
* **Fedora**
    
* **openSUSE**
    
* **Linux Mint** (yeah, I know!)
    
* And even enterprise distros like **Rocky Linux** and **Red Hat Enterprise Linux (RHEL)**