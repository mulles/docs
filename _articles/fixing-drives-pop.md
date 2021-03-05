---
layout: article
title: Mount and repair file systems
description: >
    How to mount and repair common file system issues.
keywords:
  - Repair
  - File System
  - Pop!_OS
hidden: false
section: pop

---

## Problem

File Systems can be damaged from events like unexpected power loss or unsafe removal of drive(s). This is where you would run a File System repair tool on your system. There are a few ways to do this and we'll list them below:

## Solution

### GUI (Graphical User Interface)

We can use the Disks application once the drive (on the left side) is selected. From there click on the partiton (Pop uses Ext4 for the root partition) then the gear icon for the menu in the below screenshot:

![Disks-Repair](/images/fixing-drives/disks-application.png)

### CLI (Command Line Interace)

We can instead use the <u>Terminal</u> application to perform the same behavior using these commands depending on your drive:

|         SATA          |           NVMe            |
|:---------------------:|:-------------------------:|
| sudo fsck -y /dev/sda | sudo fsck -y /dev/nvme0n1 |