# Transform Your Old Laptop into Hi-Res Music Player with Daphile for Free!

Are you a music enthusiast with an old PC or laptop gathering dust? Why not breathe new life into it by transforming it into a dedicated **Hi-Res** music player? With the right software and a few simple steps, you can enjoy high-quality audio playback without spending a dime. In this guide, we'll walk you through turning your old laptop into a powerful Hi-Res music streaming device using **Daphile**, a lightweight, open-source media server and player optimized for high-fidelity audio.

![daphile_use-case](https://github.com/user-attachments/assets/f5298a41-503d-400e-940c-08381a84ff87)

### Why Use an Old Laptop for Hi-Res Music?

-	**Cost-effective**: No need to buy expensive dedicated hardware.
-	**Dedicated device**: Keeps your main computer free from music playback duties.
-	**Customizable**: Tailor the setup to your preferences.
-	**Eco-friendly**: Repurpose existing hardware instead of discarding it.

### What You'll Need?
![requirements](https://github.com/user-attachments/assets/8a75dbf7-70ec-4c2b-a21f-0ef9d2d3609d)

-	An **old laptop** with decent hardware. (at least 2GB RAM, a stable network connection).
-	A **USB DAC** (Digital-to-Analog Converter) for high-quality audio output. I will be using SMSL PS100, cheap but sounds good.
-	A **USB drive** or **SD card**.
-	**Internet connection** for downloading necessary software.
-	Basic familiarity with BIOS/UEFI settings and network configuration.

### Step-by-Step Guide

### 1. Prepare Your Laptop

For this guide, I will be using my old Lenovo Ideapad 310 laptop (4 GB RAM with 150 GB SSD drive).

-	**Clean Install (Optional)**: For optimal performance, consider installing a lightweight Linux distribution or wiping the existing OS and installing Daphile directly.
-	**BIOS Settings**: Ensure the laptop is set to boot from USB or network if needed.
-	**Connect Hardware**: Plug in your USB DAC if available, and connect your laptop to your home network via Ethernet or Wi-Fi. In my case I will connect my laptop using ethernet cable because the built-in wireless adapter of my old laptop is not supported by daphile.

### 2. Download Daphile

Visit the official Daphile website: https://daphile.com/
Download the latest Daphile ISO image.

### 3. Create a Bootable USB Drive

Use tools like **Rufus** or **BalenaEtcher** (Windows) to create a bootable USB stick with the Daphile ISO.
Insert your USB drive, launch balenaEtcher on your machine and locate the daphile iso image in your computer. Select your USB drive as the target then click Flash. This will take 5-7 minutes depending on your machine.

![flashing_to_USB](https://github.com/user-attachments/assets/f5b8ce6c-cceb-4011-a2cf-46f171e3ae29)


### 4. Boot Your Laptop from USB

Insert the bootable USB and restart your laptop.
Access the boot menu (usually by pressing F12, F2, DEL, or ESC during startup).
Select the USB drive to boot from.

### 5. Install and Configure Daphile

Follow on-screen prompts to run Daphile in live mode or install it onto the laptop’s hard drive.

![daphile_initial_screen](https://github.com/user-attachments/assets/e8f3a93d-0376-4312-b828-b0df36275ab5)

For the initial settings you will be prompted to:

- configure wireless network (I just skip this because my wireless adapter is not supported).
- configure static IP address (I opted to configure static IP address. If you don't have knowledge on configuring static IP address, make sure to hook up the ethernet cable to your old laptop and let the DHCP of your router assign the IP address dynamically.
- wipe/prepare another storage device as a Daphile installation target (This will simply format the hardrive of your old laptop).

After Daphile has finished starting up, you should see the following message displayed on your screen. You will need the IP address that shown on this screen or the static IP address that you configure earlier to access the device using web browser.

![Daphile_screen](https://github.com/user-attachments/assets/7db276fb-34e9-4b9c-a527-d564c21afc3c)

Access the Daphile web interface via another device on the same network by entering the laptop's IP address in a browser. 

![Daphile_installation](https://github.com/user-attachments/assets/4aad9900-fac9-4626-ac93-30cc4cdcd111)

On the Settings > System Firmware > New Installation, the local hardrive of your laptop will show up here, select it. For the Partition table just keep MSDOS as it offer better compatibility with PC BIOS. The boot loader slection may vary depending on your laptop, but in most cases just select BIOS and UEFI. For MAC computers it is recommended to select UEFI boot loader only. 
### 6. Set Up Music Library

In this set up I will utilize the extra storage available on the hard drive. In the General tab > Media server selection, select internal. If you have NAS (Network Attached Storage) you can select external then provide the IP address of your NAS. 

![daphile_media-server2](https://github.com/user-attachments/assets/bef07bf1-1b9a-4fc0-b759-53a22e83540a)

I leave the Storage configuration as default. Daphile uses DaphileData partition as your audio files storage, but you can customize this if you want it to save to other location.

![daphile_media-server1](https://github.com/user-attachments/assets/19d0e508-5be4-453e-8242-ce2a980606bc)


### 7. Configure Audio Output

Connect your USB DAC or use the built-in audio output.
In Daphile settings, select your preferred audio output device.
Test playback to ensure sound quality.

### 8. Control Playback

Use the Daphile web interface from your smartphone, tablet, or PC to browse and play your music.
You can also configure remote controls or integrate with apps like BubbleUPnP or Volumio for enhanced control.

### Tips for Optimal Performance

- **Use wired Ethernet** for stable streaming, especially if accessing large Hi-Res files (I use FLAC for all of my music collecions).
- **Regularly update Daphile** for new features and security patches.
- **Invest in a good USB DAC** for the best Hi-Res audio quality.

### Enjoy Your Hi-Res Music!

With your old laptop now transformed into a dedicated Hi-Res music player, Bitperfect and gapless playback, and enjoy your high-fidelity audio library anytime. Whether you’re relaxing at home or hosting friends, this setup offers a cost-effective, eco-friendly way to indulge in premium sound quality.

