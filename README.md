# hyprland

obs: for Hyperland

instal git yay

git clone https://aur/archlinux.org/yay-git.git
cd yay-git
makepkg -si


yay -S hyprland hyprpaper wofi terminator waybar tt-font-awesome



## Waybar

" copy from /etc/xdg "

cp /etc/xdg/waybar/config ~/.config/waybar/config
cp /etc/xdg/waybar/style.css ~/.config/waybar


## Nvidia

yay -S linux-headers nvidia-dkms qt5-wayland qt5ct libva libva-nvidia-driver-git

Add modules: nvidia nvidia_modeset nvidia_uvm nvidia_drm to /etc/mkinitcpio.conf

Generate new image: sudo mkinitcpio --config /etc/mkinitcpio.conf --generate /boot/initramfs-custom.img

Add/create the following: options nvidia-drm modeset=1 in /etc/modprobe.d/nvidia.conf

reboot!