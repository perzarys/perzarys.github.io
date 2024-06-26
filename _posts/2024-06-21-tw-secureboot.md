---
layout: post
title: "openSUSE Tumbleweed: A drawback of secure boot"
tags: opensuse tumbleweed secure-boot
categories: opensuse
excerpt: Having secure boot enabled yields nice reports in system settings. Oh, and it might be useful privacy-wise. But it comes at a cost.
---

Having secure boot enabled yields nice reports in system settings. Oh, and it might be useful privacy-wise. But it comes at a cost. 

The convinience of automated BIOS updates on openSUSE is limited by Secure Boot. Software manager will propose to reboot to install BIOS/firmware updates, and after reboot will indicate that the updates were successful. However, when Secure Boot is on, the updates won't actually install. They will reappear in the Software manager as if they were never downloaded or installed. 

To solve this issue, disable Secure Boot temporarily in the BIOS, boot the system, install the firmware updates, reboot and let the BIOS flasher do its thing. Then, check if the update was applied by comparing the BIOS version with the most recent currently available version for your device, and if everything is fine, you can re-enable Secure Boot in the BIOS and boot your system as usual. Repeat the process each time a new BIOS update is available.

This problem is also addressed [here](https://blog.paranoidpenguin.net/2024/03/opensuse-tumbleweed-needs-to-fix-secure-boot/), if you want to get into more detail.