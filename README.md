> [!NOTE]
> Alex (the creator of PearOS) is already working on an ARM version. 
<div align='center'>
<p align="center">
  <img width="300" height="300" src="https://github.com/user-attachments/assets/c6bec808-b8b5-42a6-a459-e05656e47c3c" />
  </p>
<img src='https://img.shields.io/github/v/release/pearOS-archlinux/iso?color=%23FDD835&label=version&style=for-the-badge'>

</a>
  
<img src='https://img.shields.io/github/license/pearOS-archlinux/iso?style=for-the-badge'>
  
</a>

  <p><a href="https://discord.gg/QJPetvVhUb"><img alt="Discord" src="https://discordapp.com/api/guilds/697456171631509515/widget.png?style=banner2"?link=https://discord.gg/yp4xpZeAgW&link=https://discord.gg/yp4xpZeAgW> </a></p>
  
</div>

<br />

---

# pearOS-arch-base 📌
It is pearOS, but with Arch Base. Yes! It uses vanilla arch, less bugs, easier, better etc.

## Why? 📌
I had enough with debian-based distros.
pearOS with arch base, solve some of the big problems with pearOS, for example:

> "this require you to reinstall with every new release"

> "sudo apt upgrade would/will destroy your installation"

Not anymore. With arch, there no more base-hopping
Now, with arch, the system is now Rolling Release, as it should be :>

You can do now `sudo pacman -Syu` and you will stil have the pearOS branding.

## Ok... How do I build it? 📌
Make sure you satisfy the dependencies in the section below.
After that, run `sudo ./build-binary` and ~~pray~~ wait.

**Note:** The build script must be run as root (using `sudo`) since it needs to create chroot environments and install packages.

### Dependencies: 📌

#### Required packages:
```sh
# Core build tools
sudo pacman -S arch-install-scripts    # Provides pacstrap and arch-chroot
sudo pacman -S mtools                  # Provides mcopy, mmd for FAT filesystem operations
sudo pacman -S squashfs-tools          # Provides mksquashfs for creating squashfs images
sudo pacman -S xorriso                 # Creates the final ISO image
sudo pacman -S e2fsprogs               # Provides mkfs.ext4 and tune2fs for filesystem creation
sudo pacman -S git                     # Required for cloning pearOS-installer during build
sudo pacman -S pv                      # Required to see progress bars
