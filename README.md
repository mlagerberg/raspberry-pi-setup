Raspberry Pi Guide
===

*A guide to stuff you might want to do when you get your Raspberry Pi, stuff that you otherwise might forget to do, or stuff that is a pain to do when you find out you should have done them earlier.*

Disclaimer: I'm not a Raspberry Pi guru, or even someone who knows a lot about Linux in general, but when I got my Pi I had to figure out many things about both that would be a waste for any other non-guru to also figure out for themselves. So here they are, jotted down for your and my future reference.

I'm assuming a freshly installed **Raspbian** image, although other Debian-based versions shouldn't be much different.


## Table of Content

### 0. Preparation

1. [Hardware][0.1]: know before you go
2. [SD card][0.2]: prepare the SD card for 'headless' set-up (no display)

[0.1]: ./0.1-hardware.md
[0.2]: ./0.2-sd-card.md

### 1. First boot

Keep your monitor and keyboard attached to the Pi until you've done this part.

1. [Before anything else][1.1]: making sure the entire SD card is used, update everything.
2. [WiFi][1.2]: configure WiFi, set a static IP address, troubleshoot missing networks on the Pi 3.
3. [Basic security][1.3]: disable root over SSH, change default password.

[1.1]: ./1.1-before-anything-else.md
[1.2]: ./1.2-wifi.md
[1.3]: ./1.3-ssh.md

### 2. Network security

Set up a firewall using iptables and automate blocking of suspicious activity using fail2ban.

1. [Firewall][2.1] (iptables)
2. [Auto-block login attempts][2.2] (fail2ban)
3. [Two-factor authentication][2.3]
4. [Other network security tools][2.4] (netstat, iftop)

[2.1]: ./2.1-iptables.md
[2.2]: ./2.2-fail2ban.md
[2.3]: ./2.3-two-factor-authentication.md
[2.4]: ./2.4-security-tools.md


### 3. Common uses

Some common things to do with a Raspberry Pi.

1. [Remote desktop][3.1]
2. [External storage][3.2]: attach external NTFS drive to usb port, includes troubleshooting.
3. [Periodic backups][3.3]: backup the entire SD card to external storage, and use cron.
4. [HDMI output][3.4]: keep HDMI always on, disable screensaver, fix HDMI audio, boot to website in kiosk mode.
5. [Some useful commands][3.5]
 
[3.1]: ./3.1-remote-desktop.md
[3.2]: ./3.2-external-storage.md
[3.3]: ./3.3-periodic-backups.md
[3.4]: ./3.4-HDMI-output.md
[3.5]: ./3.5-analog-video-output.md
[3.6]: ./3.6-some-useful-commands.md

### 4. Specific apps and devices

Instructions on installing/building/configuring some specific apps.

1. [Resilio Sync][4.1] (formerly BitTorrent Sync): self-hosted cloud storage
2. [Webcam + Motion][4.2]: security camera
3. [Git][4.3]
4. [Bluetooth keyboard][4.4]
5. [Privoxy, OpenVPN][4.5]: proxy and vpn
6. [gPhoto2][4.6]: control a usb-connected digital camera

[4.1]: ./4.1-btsync.md
[4.2]: ./4.2-motion.md
[4.3]: ./4.3-git.md
[4.4]: ./4.4-bluetooth-keyboard.md
[4.5]: ./4.5-proxy-vpn.md
[4.6]: ./4.6-gphoto2.md

### 5. Controlling the RPi

Information on controlling the Raspberry Pi's hardware features.

1. [Minimize power consumption][5.1]
2. [Control LEDs][5.2]

[5.1]: ./5.1-power-consumption.md
[5.2]: ./5.2-leds.md
