# varch
arch installation info

#use btrfs , luks v.2 , manually erase partition if windows exists :), minimal , *multilib

vim /etc/pacman.conf #paralleldownload=10 ; ILoveCandy
pacman -Sy
pacman-key --init
pacman-key --populate

#addditional pakages
#git vim xdg-user-dirs xdg-user-dirs-gtk nvidia nvidia-dkms nvidia-settings nvidia-utils linux-headers #neofetch :')

#after installation add nvidia modules
vim /etc/mkinitcpio.conf #modules={nvidia nvidia_modeset nvidia_uvm nvidia_drm i915}
#populate modules
mkinitcpio -P #check for error resolve b4 boot
#pacman -S os-prober #regenerate

#yay/paru+ installation 
git clone https://aur.archlinux.org/yay-git.git #sudo chown -R vinodambatt:vinodambatt ./yay-git ::ls -l
cd yay-git
makepkg -si

sudo usermod -c "Vinod Ambatt" vinodambatt #;)

pacman -S --needed -xfce xfce-goodies #xfce install
pacman -S network-manager-applet bluez bluez-utils blueman #network manager applet and bluetooth tools
#wicd
sudo systemctl enable bluetooth.service #start service n boot
pacman -S gvfs gvfs-mtp #mtp support
pacman -S pavucontrol #volume control

yay librewolf #browser
yay hblock #ad block
yay ufw #firewall
yay yuzu #switch emulator
yay protonvpn-cli #vpn
yay peazip variety gparted timeshift missioncontrol # archive manager , wallpaper , diskpartition, system restore, taskmgr
#add font and thems icons as per mood
#firacode , dark-theme ,
# remove unnecessary shortcut keys from keyboard :settings,Change power manager ,mouse theme,use mouse emulator on accessibility,windows manager tweaks,settings:windows manager

#links for help

