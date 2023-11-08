# How to use nmtui (NetworkManager) to connect to WPA2 Enterprise Networks
A no frills methods to connect to WPA2 Enterprise Networks or Wi-Fi with a username and password using nmtui (NetworkManager)

This guide will help you connect to a WPA2 Enterprise secured WiFi network using nmtui and nm-connection-editor on Linux systems such as Arch or Artix.

## Prerequisites
Before you begin, ensure you have nmtui installed and working properly. There are many guides available online to help you with this.
Also keep in mind im trying to connnect to Western Michigans WMU Secure Wifi. You may have something similar.

## Steps
1. Install nm-connection-editor
For Arch or Artix Linux, use the following command to install nm-connection-editor:

```bash
sudo pacman -S nm-connection-editor
```
2. Launch nm-connection-editor
Run the following command to start nm-connection-editor:

```bash
sudo nm-connection-editor
```
3. Create a New Connection
Click the + icon in the bottom left corner.
Set the Connection name as you prefer.
For SSID, enter the WiFi network's SSID (e.g., WMU Secure).
Set Mode to Client.
Set Band to Automatic.
The Device should default to your current device. Confirm this with ip link.
### Important: In the Cloned MAC address section, set it to preserve. Some WiFi networks may not accept a random MAC address.

4. Configure WiFi Security
Use the settings provided by your WiFi network provider.
For Security, select WPA2 Enterprise.
Authentication: Choose PEAP.
Domain: Enter the domain provided by your WiFi provider (e.g., secure.wireless.wmich.edu).
### Important: Check the option No CA certificate is required (if applicable for your network). Without this, the connection may not work.
Enter your Username and Password.
After completing these steps, your setup should be complete, and you should be able to connect to the WPA2 Enterprise WiFi network.

## For reference here is my schools page on how to connect to the wifi


![Screenshot 2023-11-08 153631](https://github.com/VEETS5/nmtui-WPA2EnterpriseConnectionTutorial/assets/20433885/49282c39-e33e-4cb5-9647-033fee90c8f7)
