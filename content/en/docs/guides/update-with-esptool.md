---
title: "Update Your USB Nugget with ESPtool"
description: "Flash your RubberNugget via the command line"
lead: "Flash your RubberNugget via the command line"
date: 2020-10-13T15:21:01+02:00
lastmod: 2020-10-13T15:21:01+02:00
draft: false
images: []
menu:
  docs:
    parent: "guides"
weight: 110
toc: true
---
{{< alert icon="ℹ️" context="info" text="<b>Update First:</b> The USB Nugget is updated frequently. Get the latest version to ensure you have access to new features & bug fixes!" />}}

If you're more comfortable in the command line (or just hate using Chrome), you can also update your nugget using [ESPtool](https://github.com/espressif/esptool).

**Step 1: Visit the [release page](https://github.com/HakCat-Tech/RubberNugget/releases) & download the most recent .BIN file.**

**Step 2: On the back of your Nugget, locate the "0" button & hold it down.**

<img src="/images/RubberNugget-Back-Purple.png" title="Nugget Image"/>
<br /><br />

**Step 3: Plug the Nugget into your computer with a USB  cable & then release the "0" button.**

<em>This puts the nugget into flashing mode. 
If you have issues with step 5, try holding down the "0" button, tapping the "RST" button, and then releasing the "0" button to enter flashing mode instead.</em>

**Step 4: Find the serial port your Nugget is connected to.**
Run the command below to erase the flash of your Nugget, making sure to replace "SERIAL_PORT" with the port the serial port your Nugget is connected to. 

- **Windows**

Found via Device Manager

- **MacOS**
```bash
ls /dev/cu*
```
- **Linux**
```bash
ls /dev/tty*
```

**Step 5: Erase the Nugget's flash memory**

Make sure to replace SERIAL_PORT, with the serial port of your Nugget.

- **Windows**
```bash
esptool --chip esp32s2 -p SERIAL_PORT erase_flash
```
- **Mac**
```bash
esptool.py --chip esp32s2 -p SERIAL_PORT erase_flash
```
- **Linux**
```bash
esptool.py --chip esp32s2 -p SERIAL_PORT erase_flash
```

**Step 6: Flash the new firmware .BIN file**

After erasing is complete, run the following command, making sure to replace SERIAL_PORT with the port your Nugget is on, and UPDATE.BIN with the update file.

- **Windows**
```bash
esptool --chip esp32s2 -p SERIAL_PORT write_flash -z 0x1000 UPDATE.BIN
```
- **Mac**
```bash
esptool.py --chip esp32s2 -p SERIAL_PORT write_flash -z 0x1000 UPDATE.BIN
```
- **Linux**
```bash
esptool.py --chip esp32s2 -p SERIAL_PORT write_flash -z 0x1000 UPDATE.BIN
```

Once flashing is finished, unplug your Nugget to complete the update.

#### That's it! Your Nugget is ready to hack.

Plug in your USB Nugget and watch it mount as a flash drive. You can open the drive to explore preinstalled payloads and begin to add your own.

You can also connect via the web interface and run payloads from any device! The network name is **RubberNugget** and the password is **nugget123** to connect. Once connected, navigate to `192.168.4.1` in a browser.