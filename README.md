# Hogwarts Grub-2-theme

> This project is BEING improved, please waiting for updates! 🙇‍♂️>>👨‍🔬🔧

This is a theme plugin for grub 2 boot GUI. You can also install it on ventoy (vtoy) USB device.

## Project Structure

+ D **/background** - Background images.
+ D **/commen** - Configuration text files and font family files.
+ D **/assets** - OS icons.
+ D **/dist** - Export directory.
+ F **/runme.sh** - Utilities for installation, export and option.
+ F **/README.md** - This help document.

## Installation method

### Automatically Install - How to Use Runme

```bash
chmod +x ./runme.sh
./runme.sh <option> [selection]
```

+   **option:**

    -   **install**

    -   **export**

    -   **vtoy**

+   **selection:**

    -   **-s | --os**

    -   **-o | --path**

### Manually Install

1.  replease default background image in **/background.png** your favorite image in **/background/*.png**

    `cp ./background/HERE.png ./background`

2.  

**Install to GNU/Linux** (Following Above)

3.  Merge your configuration.

    `sudo nano /etc/default/grub`

    Add the fowllowing text in the end.

    ```plain/text
    # GRUB_TERMINAL=console # Check that this property has been commented.
    GRUB_THEME="/boot/grub/themes/>>>FILL WITH YOUR REAL PATH<<</theme.txt"
    GRUB_GFXMODE=1920x1080x32
    ```

4.  Update to grub.
    
    - Debian / Ubuntu

        `sudo update-grub`

    - Fedora / RHEL / Red Hat

        `sudo grub2-mkconfig -o /boot/grub2/grub.cfg`

    - Arch

        `sudo grub-mkconfig -o /boot/grub/grub.cfg`

**Install to Ventoy SUB Device** (Following Above)


