## Dzen2 config files (ARCH/XFCE)

**strangeWORLD**
![screenshot](https://github.com/Ksiencha/Dzen2/blob/master/Screenshot.png)

* [PREREQUISITES](https://github.com/Ksiencha/Dzen2/blob/master/README.md#prerequisites)
* [INSTALLATION](https://github.com/Ksiencha/Dzen2/blob/master/README.md#installation)

### PREREQUISITES
---
#### 1. CPU Temperature

    $ sudo pacman -S i2c-tools
    $ sudo sensors-detect       # Answer 'y' on every question
    $ sensors

#### 2. Battery state

    $ sudo pacman -S acpi
    $ acpi -V

#### 3. Wget tool

    $ sudo pacman -S wget

#### 4. Checking current keayboard layout in use

    $ yaourt -S xkblayout-state

#### 5. Install calculator

    $ sudo pacman -S bc

#### 6. Install JSON-parsers 
6.1. Install jq parser (read the Install file in folder JSON-parser)
6.2. Insall jshon parser

    $ sudo pacman -S jshon

#### 7. Fonts

You can find them in **Fonts** directory:

* Inconsolata
* Ubuntu
* Meslo LG S DZ
* FontAwesome (http://fortawesome.github.io/Font-Awesome/)
* Ionicons (http://ionicons.com/)
* Typicons (http://www.typicons.com/)
* Weather Icons (https://github.com/erikflowers/weather-icons)

**Note!**

If you want to download the latest version of **Ionicons** font from the official website there will be no Pacman and Arch icons. The **Fonts** directory contains the patched version of this font with mentioned icons.


### INSTALLATION
---

#### 1. Install dzen2

    $ sudo pacman -S dzen2

#### 2. Place your Dzen2 folder into your `/home/username` directory
#### 3. Make all `.sh` files executable

    $ cd ~/Dzen2/dzen-configs/strangeWORLD
    $ sudo cp dzen_start /bin/
    $ sudo chmod +x *.sh
    $ sudo chmod +x /bin/dzen_start

#### 4. Starting dzen2

**Manually start**

    $ dzen_start

**Manually stop**

    $ killall dzen2

**Automatically on boot (FOR XFCE USERS)**

Settings Manager **>>** Session and Startup **>>** Application Autostart **>>** Add

Command: `/bin/dzen_start`
