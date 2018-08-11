# AwesomeArchBase
Arch Linux installation scripts for a semi-minimal AwesomeWM ricing copycat setup courtesy of [@lcpz](https://github.com/lcpz)

## License
In the spirit of @lcpz, the scripts found here are released under the same [Creative Commons BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) 
license. 

## About
After having to setup Arch Linux numerous times on several machines - some of which are over a decade old, and having found a combination of window manager (_**[awesomeWM](https://github.com/awesomeWM/awesome)**_) and desktop environment (_**[XFCE](https://xfce.org)**_) I *liked* most for ease of customization and minimal system resource demands, I have finally taking to document the procedures for future reference, as well as produced scripts to aid in automating much of the process. Why? The most obvious, to save time of dealing with maticulously finding and setting the exact preferences and/or transferring specific files manually. Additionally, since much of the installation requires internet, tapping a GitHub repository provides an opportunity to learn the ins and outs of a new skillset I was in dire need of expanding. Lastly, data organization. I'm a packrat for all things digital, and syncronization means "put it on my desktop" unfortunately. But alas, I'm working to correct this as it's been a long time coming, please pardon my digital mess as it spills into GitHub as bmyte commits.

## What's Here
- [x] README
- [ ] Initial Arch install helper scripts [archinstall.sh]
  - [ ] verifies boot mode (BIOS/EFI)
  - [ ] establish Internet connection (ethernet DHCP) and setup NTP time service
  - [ ] guided disk partitioning (fdisk and mkfs wrapper) w/ SWAP options
  - [ ] mount and pacstrap install base/base-devel & ntfs-3g (with preset additions or custom specified ones)
  - [ ] generate filesystem table (fstab)
  - [ ] chroot with Arch setup helper script (arch-chroot)
    - [ ] **chroot Arch setup helper script** [archsetup.sh]
    - [ ] choose timezone (local/UTC)
    - [ ] generate locales and set LANG variable (UTF-8)
    - [ ] set hostname w/ permanent IP option for hosts
    - [ ] make init RAM filesystem (mkinitcpio -p linux)
    - [ ] set root password (passwd)
    - [ ] install GRUB bootloader (grub2)
- [ ] Post-Installation Scripts
  - [ ] install sudo and allow wheel group (password/not)
  - [ ] add main admin rights user (wheel)
- [ ] Base Programs install: xorg, xorg-init, numlockx, awesome, urxvt, compton, deluge, vlc/mpv, chromium/firefox, w3m, ranger, openssh, git, curl, wget, scrot, tmux, unrar, unzip, p7zip, youtube-viewer/-dl, poppler, mediainfo, gimp
- [ ] Essential Programs ("Bulking"): filezilla, finch, hexchat, mumble/umurmur, links, gpo/gpodder, mutt/neomutt, ttf-inconsolata, arandr, ffmpeg, mpd/mpc, ncmpcpp, pulseaudio/-alsa, pamixer/pulsemixer
- [ ] AUR yay! setup and more base programs: discord, retroshare
- [ ] Laptop/WiFi -> NetworkManager (networkmanager, network-manager-applet)
- [ ] Copy the Cats w/ bmyte's themes and rc.lua
- [ ] X.Files -> bmyte's own configs/dotfiles
  - [ ] .bashrc
  - [ ] .bash_profile
  - [ ] .asoundrc
  - [ ] .xinitrc
  - [ ] .Xdefaults/.Xresources
- [ ] QEMU Scripts w/ Bridge & Tap
  - [ ] netbridge.sh -> setup bridge(br0) and enable services(networkd and resolved)
  - [ ] tapnet.sh -> generates a tap for VM
  - [ ] QEMU Launch Script Templates for BIOS/OVMF
  - [ ] autostart VM systemd service template

## Thanks
I'd like to especially thank YouTubers [msjche](https://www.youtube.com/user/msjche) and [Irishluck Linux](https://www.youtube.com/channel) for really getting me into the awesome window manager. For a time I was simplying installing XFCE as it was relatively minimal on system demands, yet handled much (if not all) of my use cases and was documented well enough for some easy modifications. I have to admit before finding [Arch Linux](https://www.archlinux.org) I would actually just install Xubuntu (if even, sometimes just running it Live off a USB drive) since I never fully made the plunge to GNU/Linux. However, after recently building my own system, I decided to dive deep and setup a virtualized KVM based Windows rig with direct PCI GPU passthrough to allow near native performance, and that's right, gaming in a Windows VM. Having previously tackled the [Linux From Scratch project](http://www.linuxfromscratch.org) where I learned a great deal about GNU/Linux, I was determined to know as much about the internal functions of my host Linux distro to be as I could. In search of highly configurable and minimal Operating Systems - again, I was turned onto Arch Linux and their amazing wiki documentation for anything and everthing I could imagine! This worked well, as resources for GPU passthrough for dedicated gaming VM were rather favoring of Arch (though a good share for Fedora came up; and I suggest any of the meek whom find Arch to be tantalizing to maybe give it a shot there, as their @virtualization package is rather proficient and GUI tools for VM management can really alleviate a lot of the guesswork/research into setting up and running VMs - not that GUI tools don't exist for Arch, but I preferred to avoid the abstraction from the details and wanted even more control than was *inherently* permitted by some of the GUIs). For a much more in-depth rundown of my Windows gaming VM, checkout my GitHub repository [ArchGamingVM]() which documents the details much like this repo.

:exclamation::exclamation: **Double Special Thanks go out to [@lcpz for his Awesome WM Copycats themes](https:/github.com/lcpz/awesome-copycats) and awesome LUA framework which were the foundations of my dream OS desktop interface (opus in profectus)** :exclamation::exclamation:<br>
:exclamation::exclamation: *since starting this project, the additional find of YouTuber [LukeSmith](https://www.youtube.com/channel) and his ricing GitHub repo [LukeSmithxyz](https://github.com/LukeSmithxyz), I would like to as well add thanks to him for his inspiring workflow videos and good place to start on this automating Arch install project with his Wizards; as well as his lists of some more sexy Linux softwares and script kitty tricks with bash.* :exclamation::exclamation:

