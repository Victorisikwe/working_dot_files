# working_dot_files
just for me

```
# Using yay for AUR helper
pacman -S --needed git base-devel
git clone https://aur.archlinux.org/yay-bin.git
cd yay-bin
makepkg -si
```

```
# Installing needed dependencies
yay -S hyprland-git polkit-kde-agent dunst grimblast rofi rofi-emoji       \
wl-clipboard wf-recorder wlogout grimblast-git hyprpicker-git hyprpaper-git \
xdg-desktop-portal-hyprland-git ffmpegthumbnailer tumbler wtype colord      \
imagemagick swaylock-effects qt5-wayland qt6-wayland ripgrep waybar-hyprland-git
```

* Extras
```
# themes
yay -S catppuccin-gtk-theme-mocha catppuccin-cursors-mocha catppuccin-mocha-grub-theme-git nwg-look
```

```
# apps
yay -S cava pavucontrol ranger zsh starship neovim viewnior noise-suppression-for-voice
```

#Clone repo
```
git clone https://github.com/linuxmobile/hyprland-dots $HOME/Downloads/hyprland-dots/
cd $HOME/Downloads/hyprland-dots/
rsync -avxHAXP --exclude '.git*' .* ~/
```

```
#As fonts i'm using Cartograph CF (patched with nerdfont) It's a licensed font, then select any font you like
mkdir -p $HOME/Downloads/nerdfonts/
cd $HOME/Downloads/
wget https://github.com/ryanoasis/nerd-fonts/releases/download/v2.3.1/CascadiaCode.zip
unzip '*.zip' -d $HOME/Downloads/nerdfonts/
rm -rf *.zip
sudo cp -R $HOME/Downloads/nerdfonts/ /usr/share/fonts/
```

```
# Regenerate font cache
fc-cache -rv 
```
```
# Login manager
sudo tar -xzvf ~/Downloads/sddm-sober.tar.gz -C /usr/share/sddm/themes
```

## This will extract all the files to a new folder "sober" inside of the themes directory of SDDM.
## After that you will have to point SDDM to the new theme by editing its config files :

```
vim /etc/sddm.conf.d/sddm.conf
```

In the [Theme] section set Current=sober. For a more detailed description please refer to the Arch wiki on sddm. Note that, depending on your system setup, a duplicate configuration may exist in /etc/sddm.conf. Usually this takes preference so you want to set the above line in this file if you have it.

