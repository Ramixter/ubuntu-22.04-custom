# Ubuntu 22.04 Customization

## Installing dependencies & Updates

```bash
sudo apt update
sudo apt full-upgrade
sudo apt install gnome-tweaks
sudo apt install gnome-shell-extensions
sudo apt install curl wget git jq
```

> NOTE: Optional
> ```bash
> sudo apt install conky-all
> sudo apt install lua5.3
> sudo add-apt-repository ppa:teejee2008/foss
> sudo apt update
> sudo apt install conky-manager2
> ```

## Gnome extensions:

wWe have to go to [https://extensions.gnome.org/](https://extensions.gnome.org/) and do the changes to set up the *Gnome Extensions*:

![img](images/img1.png)

Now we restart the Operating System so that the changes are applied correctly. We can do it through GUI or with the command:

```bash
sudo reboot
```

## Download resources

We need this resources:

- [WhiteSur-gtk-theme-master.zip](resources/WhiteSur-gtk-theme-master.zip)
- [Reversal-icon-theme-master.zip](resources/Reversal-icon-theme-master.zip)
- [Vimix-cursors-master.zip](resources/Vimix-cursors-master.zip.zip)
- [media-controls-main.zip](resources/media-controls-main.zip)

- [arcmenu-config.zip](resources/arcmenu-config.zip)
- [conky-config.zip](resources/conky-config.zip)
- [dash-to-panel-config.zip](resources/dash-to-panel-config.zip)
- [extensions.zip](resources/extensions.zip)
- [fonts.zip](resources/fonts.zip)
- [media-control-config.zip](resources/media-control-config.zip)
- [wallpapers-pack.zip](resources/wallpapers-pack.zip)
- [all-extensions-config.zip](resources/all-extensions-config.zip)

### Cloning repository:

```bash
git clone https://github.com/Ramixter/ubuntu-22.04-custom.git
cd ubuntu-22.04-custom/
```

### Unzip resources:

> We will have to go to the repository where we have copied the github repository

```bash
# cd ubuntu-22.04-custom/
unzip resources/WhiteSur-gtk-theme-master.zip -d resources/
unzip resources/Reversal-icon-theme-master.zip -d resources/
unzip resources/Vimix-cursors-master.zip -d resources/
unzip resources/media-controls-main.zip -d resources/
unzip resources/arcmenu-config.zip -d resources/
unzip resources/conky-config.zip -d resources/
unzip resources/dash-to-panel-config.zip -d resources/
unzip resources/extensions.zip -d resources/
unzip resources/fonts.zip -d resources/
unzip resources/media-control-config.zip -d resources/
unzip resources/wallpapers-pack.zip -d resources/
unzip resources/all-extensions-config.zip -d resources/
```

### Installing some resources:

> We will have to go to the repository where we have copied the github repository

```bash
# cd ubuntu-22.04-custom/

## Installing WhiteSur-gtk-theme-master
cd resources/WhiteSur-gtk-theme-master/
./install.sh -t red
# ./install.sh
cd ../..

## Installing Reversal-icon-theme-master
cd resources/Reversal-icon-theme-master/
./install.sh -red
# ./install.sh
cd ../..

## Installing Fonts
cp -r resources/fonts ~/.local/share

## Installing Vimix-cursors-master
cd resources/Vimix-cursors-master/
./install.sh
cd ../..

### Vimix-cursors-master
mkdir -p $HOME/.icons
rm -rf ~/.icons/Vimix-cursors
rm -rf ~/.icons/Vimix-white-cursors
mv ~/.local/share/icons/Vimix-cursors ~/.icons
mv ~/.local/share/icons/Vimix-white-cursors ~/.icons

## Installing Extensions
cd resources/extensions/
mkdir -p ~/.local/share/gnome-shell/extensions
cp -r * ~/.local/share/gnome-shell/extensions
cd ../..
```

Now we restart the Operating System so that the changes are applied correctly. We can do it through GUI or with the command:

```bash
sudo reboot
```

## Configuring Theme:

### Extensions

> After restarting, it may ask us to log in again so that the changes can be applied:
> ![img](images/img2-1.png)

Now we will have to configure the extensions that we have installed previously.

![img](images/img2.png)

> Note: check that *Gnome extensions* and the other extensions are turned on
> ![img](images/img4.png)

### Media Controls

> We will have to go to the repository where we have copied the github repository to copy the `media-controls-main` file into the directory `.local/share/gnome-shell/extension/`, and we will have to name it `mediacontrols @cliffniff.github.com`

```bash
# cd ubuntu-22.04-custom/
cp -r resources/media-controls-main/ ~/.local/share/gnome-shell/extensions/mediacontrols@cliffniff.github.com
```

Now we restart the Operating System so that the changes are applied correctly. We can do it through GUI or with the command:

```bash
sudo reboot
```

### All extensions config

> We will have to go to the repository where we have copied the github repository

```bash
# cd ubuntu-22.04-custom/
cd resources/all_extensions_config/
dconf load /org/gnome/shell/extensions/< all_extension_settings.conf
```

Now we restart the Operating System so that the changes are applied correctly. We can do it through GUI or with the command:

```bash
sudo reboot
```

## OPTIONAL - Setting up Icons and Fonts

This section is optional since we can change the fonts and icons if we want them to look different.

![img](images/img5.png)

## Install and config Conky

```bash
sudo apt install conky-all curl jq
mkdir -p $HOME/.config/conky
mkdir -p $HOME/.config/autostart
```

> We will have to go to the repository where we have copied the github repository

```bash
# cd ubuntu-22.04-custom/
cp -r resources/conky_config/Graffias ~/.config/conky/
cp -r resources/conky_config/start_conky.desktop ~/.config/autostart/
```

We will check that it has been applied with *Tweaks*.

![img](images/img6.png)

Now we restart the Operating System so that the changes are applied correctly. We can do it through GUI or with the command:

```bash
sudo reboot
```


7d2730483b9376ef791c604708b7aaef

daee515212ac51440b2da25fcd248a46

{execi 300 curl -s "http://weather.yahooapis.com/forecastrss?w=44418&u=c" -o ~/.cache/weather.xml}


{execi 300 curl -s "http://weather.yahooapis.com/forecastrss?w=2295411&u=c" -o ~/.cache/weather.xml}

{execi 300 wget "http://weather.yahooapis.com/forecastrss?w=2295411&u=c" --output-document=.cache/weather.xml}
