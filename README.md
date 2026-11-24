# GhostKit OS (`0827-22-00`)

Custom Debian Trixie + XFCE live-build configuration featuring:
- **Version:** `0827-22-00` (`OS : GhostKit`)
- **Desktop:** XFCE with custom GhostKit branding, banner, and Security sub-menus
- **Tools:** LibreWolf (isolated profile launcher), Tor Browser, Telegram client, and Wireshark/tshark (`dumpcap` capabilities + menu wrapper)
- **Default Live Session:** `live` user (`ghost` password) with LightDM autologin

## Build ISO
```bash
sudo lb config \
  --distribution trixie \
  --architectures amd64 \
  --linux-flavours amd64 \
  --archive-areas "main contrib non-free non-free-firmware" \
  --bootappend-live "boot=live components username=live quiet splash" \
  --debian-installer live \
  --debian-installer-gui true \
  --iso-application "GhostKit OS 0827-22-00" \
  --iso-publisher "GhostKit" \
  --iso-volume "GHOSTKIT_0827_22"

sudo lb build
