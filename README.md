# Signageful Player Snap

As Signageful is a 100% web-based solution, it can be run on any device that has a web browser. However, if you want to utilize the full potential of Signageful, you should use the Signageful Electron Player Wrapper.


## Installation

Install an Ubuntu Core 22 image on your device. You can find the latest image here: https://cdimage.ubuntu.com/ubuntu-core/22/stable/current/
You should setup your network and user account during the installation process, so you can login to your device.

**Install Ubuntu Frame**

Ubuntu Frame is a full-screen wayland window manager that is optimized for kiosk use. It is available in the Ubuntu Store. You can install it by running the following command:

```bash
sudo snap install ubuntu-frame
```

**Install Signageful Electron Player Wrapper**

The Signageful Electron Player Wrapper is also available in the Ubuntu Store. You can install it by running the following command:

```bash
sudo snap install signageful-player-wayland
```

To quieten log spam please connect the interfaces below

```bash
sudo snap connect signageful-player-wayland:hardware-observe
sudo snap connect signageful-player-wayland:process-control
```

### Audio

To enable audio, you need to connect the pulseaudio interface:

```bash
snap install --beta pulseaudio
sudo snap connect signageful-player-wayland:pulseaudio
```

Now restart the signageful-player-wayland snap:

```bash
sudo snap restart signageful-player-wayland
```
