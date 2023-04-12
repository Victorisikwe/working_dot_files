# working_dot_files
just for me

# Using yay for AUR helper
pacman -S --needed git base-devel
git clone https://aur.archlinux.org/yay-bin.git
cd yay-bin
makepkg -si

# Installing needed dependencies
yay -S hyprland-git polkit-kde-agent dunst grimblast rofi rofi-emoji       \
wl-clipboard wf-recorder wlogout grimblast-git hyprpicker-git hyprpaper-git \
xdg-desktop-portal-hyprland-git ffmpegthumbnailer tumbler wtype colord      \
imagemagick swaylock-effects qt5-wayland qt6-wayland ripgrep waybar-hyprland-git

* Extras
# themes
yay -S catppuccin-gtk-theme-mocha catppuccin-cursors-mocha catppuccin-mocha-grub-theme-git nwg-look

# apps
yay -S cava pavucontrol ranger zsh starship neovim viewnior noise-suppression-for-voice

#As fonts i'm using Cartograph CF (patched with nerdfont) It's a licensed font, then select any font you like
mkdir -p $HOME/Downloads/nerdfonts/
cd $HOME/Downloads/
wget https://github.com/ryanoasis/nerd-fonts/releases/download/v2.3.1/CascadiaCode.zip
unzip '*.zip' -d $HOME/Downloads/nerdfonts/
rm -rf *.zip
sudo cp -R $HOME/Downloads/nerdfonts/ /usr/share/fonts/

# Regenerate font cache
fc-cache -rv 
