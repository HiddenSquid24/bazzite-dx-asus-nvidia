# Bazzite Developer Edition on Asus ROG with Nvidia Graphics

[![Build](https://github.com/HiddenSquid24/bazzite-dx-asus-nvidia/actions/workflows/build.yml/badge.svg)](https://github.com//HiddenSquid24/bazzite-dx-asus-nvidia/actions/workflows/build.yml)

This is just bazzite, but with extra developer-specific tooling, aiming to match [Bluefin DX](https://docs.projectbluefin.io/bluefin-dx/) and [Aurora DX](https://docs.getaurora.dev/dx/aurora-dx-intro) in functionality

## Installation

To rebase an existing Bazzite installation to Bazzite DX, use one of the following commands based on your current variant:

### NVIDIA Variants

**For KDE Plasma with NVIDIA:**
```bash
rpm-ostree rebase ostree-image-signed:docker://ghcr.io/HiddenSquid24/bazzite-dx-asus-nvidia:stable
```

To skip signature verification (not recommended unless you know what you're doing and why you're doing it), replace `ostree-image-signed:docker://ghcr.io` with `ostree-unverified-registry:ghcr.io`.

### ⚠️ Important Desktop Environment Warning

**Do not switch between GNOME and KDE variants!** If you are currently running:
- **GNOME** (bazzite-gnome*): Only use the `-gnome` variants above
- **KDE Plasma** (standard bazzite): Only use the variants without `-gnome` in the name

Switching between desktop environments via rebase can break your installation and may require a complete reinstall.

After running the rebase command, reboot your system to complete the installation. 

## Acknowledgments

This project is built upon the work from [amyos](https://github.com/astrovm/amyos) and [bazzite-dx](https://github.com//ublue-os/bazzite-dx)

