---
title: "Update Your USB Nugget with Chrome Browser"
description: "Flash your RubberNugget with the latest firmware"
lead: "Flash your RubberNugget with the latest firmware"
date: 2020-10-13T15:21:01+02:00
lastmod: 2020-10-13T15:21:01+02:00
draft: false
images: []
menu:
  docs:
    parent: "guides"
weight: 100
toc: true
---

{{< alert icon="ℹ️" context="info" text="<b>Update First:</b> The USB Nugget is updated frequently. Get the latest version to ensure you have access to new features & bug fixes!" />}}

Before you start hacking with your USB Nugget, make sure to update it to the latest firmware.

To update your USB Nugget, you will need:
- **A USB type C cable that supports data**
- **The [Google Chrome](https://www.google.com/chrome) web browser**
- **The latest USB Nugget firmware .BIN file**

### Flashing Via Chrome Browser
The easiest way to flash your USB Nugget is via the Chrome web browser. First, remove any case and unplug your Nugget.

**Step 1: Visit the release page & download the most recent .BIN file.**

**Step 2: On the back of your Nugget, locate the "0" button & hold it down.**

<img src="/images/RubberNugget-Back-Purple.png" title="Nugget Image"/>
<br /><br />

**Step 3: Plug the Nugget into your computer with a USB  cable & then release the "0" button.**

<em>This puts the nugget into flashing mode. 

If you have issues with step 5, try holding down the "0" button, tapping the "RST" button, and then releasing the "0" button to enter flashing mode instead.</em>

**Step 4: In a Chrome browser window, navigate to [https://nabucasa.github.io/esp-web-flasher/](https://nabucasa.github.io/esp-web-flasher/)**

<em>Currently, Firefox and other browsers do not support WebSerial.</em>

<img src="/images/esp_1.png" title="ESP Web Flasher Image"/>
<br /><br />

**Step 5: Click the "Connect" button & select the "ESP32-S2" board.**

<img src="/images/esp_web_2.png" title="ESP Web Flasher Image"/>
<br /><br />

**Step 6: Once connected, click "Erase" & confirm.**

<img src="/images/esp_web_3.png" title="ESP Web Flasher Image"/>
<br /><br />

**Step 7: After the erase is finished, click "Choose a file" & select the .BIN file from step 1.**

<img src="/images/esp_web_4.png" title="ESP Web Flasher Image"/>
<br /><br />

**Step 8: Click "Program" & wait for the .BIN to flash, then unplug to complete the update.**

#### That's it! Your Nugget is ready to hack.

Plug in your USB Nugget and watch it mount as a flash drive. You can open the drive to explore preinstalled payloads and begin to add your own.

You can also connect via the web interface and run payloads from any device! The network name is **RubberNugget** and the password is **nugget123** to connect. Once connected, navigate to `192.168.4.1` in a browser.
