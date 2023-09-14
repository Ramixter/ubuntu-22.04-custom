# Ubuntu 22.04 Customization

## Installing dependencies & Updates

```bash
sudo apt update && sudo apt full-upgrade
sudo apt install gnome-tweaks
sudo apt install gnome-shell-extensions
```

## Download resources

We need this resources:

Resources 1:

- [WhiteSur-gtk-theme-master.zip](resources/WhiteSur-gtk-theme-master.zip)
- [Reversal-icon-theme-master.zip](resources/Reversal-icon-theme-master.zip)

Resources 2:
- [arcmenu-config.zip](resources/arcmenu-config.zip)
- [conky-config.zip](resources/conky-config.zip)
- [dash-to-panel-config.zip](resources/dash-to-panel-config.zip)
- [fonts.zip](resources/fonts.zip)
- [media-control-config.zip](resources/media-control-config.zip)
- [wallpapers-pack.zip](resources/wallpapers-pack.zip)
- [all-extensions-config.zip](resources/all-extensions-config.zip)

```bash
git clone https://github.com/Ramixter/ubuntu-22.04-custom.git
cd ubuntu-22.04-custom/
# Unzip resources
unzip resources/WhiteSur-gtk-theme-master.zip -d resources/
unzip resources/Reversal-icon-theme-master.zip -d resources/
unzip resources/arcmenu-config.zip -d resources/
unzip resources/conky-config.zip -d resources/
unzip resources/dash-to-panel-config.zip -d resources/
unzip resources/fonts.zipp -d resources/
unzip resources/media-control-config.zip -d resources/
unzip resources/wallpapers-pack.zip -d resources/
unzip resources/all-extensions-config.zip -d resources/

```




