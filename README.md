complete, the concepts I learn, and the challenges I overcome. My goal is to build a clear picture of how my skills develop over time. As I grow, I’m excited to look back on these entries and see how far I’ve come.

CCNA Journey – Day 4
Lab Title: Intro to CLI


📌 Overview

Today I learned the basics of working with the Cisco Command-Line Interface (CLI) and how to connect to a router or switch using console cables like an RJ-45 rollover cable or a USB Mini-B console cable. I used a terminal emulator (PuTTY) to access the device and explored the different exec modes inside a Cisco device.

I also practiced configuring passwords, securing access, and saving device configurations—all foundational tasks for managing Cisco equipment.

🧠 What I Learned

Differences between straight-through, crossover, single-mode fiber, and multimode fiber cables

How routers, switches, PCs, and servers use different Tx/Rx port types

Why older devices required specific cables, while newer hardware supports Auto MDI-X

Basics of securing a device: setting console passwords, enable passwords, and encrypting credentials

Importance of saving configurations so they persist across reboots

🛠 Lab Details
1. Change the device hostnames

Updated the router and switch hostnames to R1 and SW1 using the hostname command in global configuration mode.

2. Configure an unencrypted enable password

Set the enable password on both devices to CCNA using enable password CCNA.

3. Test the password

Exited back to user EXEC mode and verified that the password works when entering privileged EXEC mode.

4. View the password in the running configuration

Used show running-config and saw that the password was stored in plain text.

5. Encrypt all current and future passwords

Enabled password encryption using:
service password-encryption

6. Verify encryption

Viewed the running configuration again—passwords were now encrypted using Type 7 encryption.

7. Configure a more secure encrypted enable password

Set the enable secret to Cisco:
enable secret Cisco
This creates a Type 5 (MD5) hashed password.

8. Test access again

Exited back to user EXEC mode and returned to privileged EXEC mode.
Result: Only the enable secret 'Cisco' works because it overrides the enable password.

9. View passwords and identify encryption types

Enable password (CCNA) → encrypted as Type 7

Enable secret (Cisco) → encrypted as Type 5

10. Save the configuration

Saved the running configuration to NVRAM using:
copy running-config startup-config
<img width="1860" height="855" alt="Screenshot 2025-11-29 at 9 20 14 AM" src="https://github.com/user-attachments/assets/52a0ca3a-1fab-4d18-b135-cc3b093dfb2c" />
