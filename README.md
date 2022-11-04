<div id="top"></div>

# ArchScripts

<!-- TABLE OF CONTENTS -->
<details>
  <summary>📗 <b>Table of Contents</b></summary>
  <ol>
    <li>
      <a href="#-about-the-project"> About The Project</a>
    </li>
    <li><a href="#-how-it-works">How it Works</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## 🔰 About The Project
Custom-built scripts for auto-installation of Arch Linux.

<p align="right">(<a href="#top">back to top</a>)</p>

## ⚡ How It Works

### Script descriptions
- Each script file plays a particular role:

#### Required files

- `arch_install.sh`: The main installation script.
- `config.sh`: A configuration script that runs inside *chroot*, after installing the packages.
- `env.sh`: The environment script that stores the installation/setup information.
- `printer.sh`: A printer script, mostly used to print colored messages.
- `pacman_custom.conf`: A pacman file that assumes a custom repository in `/root/pkg` when installing your system.

#### Optional files

- `expand_cowsize.sh`: Expands live available space. Useful when installing packages in the live ISO.
- `yay_install.sh`: Convenient script that allows you to install `yay` (an AUR helper) *after* installing your system.

#### Recipes
All packages are stored in each recipe, which is sourced and added to the pool of packages to install in your system.

Available recipes by default are:

#### Desktop environments
* KDE (Plasma)
* GNOME (GNOME Shell)
* i3 (Window manager)
* X11 (Minimal Xorg)

#### Bootloaders
* rEFInd
* GRUB

#### Graphic drivers
* nVidia
* AMD
* VirtualBox
* Intel
- Install Cubic
### Relevant information

The installation script (`arch_install.sh`) uses settings from the `env.sh` file, so you are required to edit it *before* installing the system!

<p align="right">(<a href="#top">back to top</a>)</p>

### Author
