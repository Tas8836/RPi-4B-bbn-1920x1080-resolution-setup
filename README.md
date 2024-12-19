# Resolution Setup for 1920x1080

This repository contains the logic to set the screen resolution to **1920x1080** at login using Budgie Desktop's **autostart feature**.
On my raspberry pi 4b running BareBoat Necessities Operating System. I had trouble with evertime I connected to a difference screen I would have to adjust something. This seems to have fixed it. 
## 📂 Files Included
| **File**                  | **Location**               | **Purpose**                              |
|--------------------------|----------------------------|------------------------------------------|
| **autostart/set_resolution.desktop**  | `~/.config/autostart/`  | Runs xrandr to set 1920x1080 on HDMI-1  |

## ⚙️ Reinstallation Instructions

### 1️⃣ **Copy the autostart file**
```bash
cp autostart/set_resolution.desktop ~/.config/autostart/

To change the screen resolution, modify the Exec= line in the autostart/set_resolution.desktop file.
Example:
Exec=/usr/bin/xrandr --output HDMI-1 --mode 1366x768

Change HDMI-1 to the name of your output (e.g., HDMI-2, DP-1, etc.) if you have multiple displays.

Restart or Log Out
You can restart your session or simply log out and log back in for the changes to take effect.
