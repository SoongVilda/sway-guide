# Sway guide
I decided to create guide how jump from KDE to Sway and more CLI environment. I hope that guide help other people with Sway useage.

## Why Sway?
I found some benefitcs of Sway - Window Managers in gerneral compare to Desktop Environment:
- Lower hardware usage: CPU, RAM, GPU
- Potential to get better battery life on laptop.
- Better gaming expericnes - fps boost, frametimes stability.
---
- [Base installation](#base-installation)
  - [Sway](#sway)
  - [Tools](#tools)
- [Base configuration](#base-configuration)
  - [Set default tools](#set-default-tools)
 
  
# Base Installation
You need to satisfy the following steps to get Sway working and to be ready for post-install configuration.

## Sway
You need install following packages
```
sudo pacman -S --needed sway swaybg swayidle swayimg swaylock wayland xorg-xwayland
```
## Tools
It would be best to choose tools like a terminal, text editor, program launcher, etc. Sway is just Window Manager. It doesn't provide a text editor or something like that.

### Terminal
You need terminal, choice is up to you. I personally prefer [Kitty](https://sw.kovidgoyal.net/kitty/)
``` 
sudo pacman -S kitty
```
> Alternative terminal: 
> - [Alacritty](https://alacritty.org/)

### Launcher
You need launcher to execute apps, program like Firefox, LibreOffice, Steam, etc. I personally prefer [wofi](https://hg.sr.ht/~scoopta/wofi)
```
sudo pacman -S wofi
```
> Alternative launcher: 
> - [Rofi](https://github.com/davatorium/rofi)

### Text editor
I personally prefer [vim](https://github.com/vim/vim)
```
sudo pacman -S vim
```
> Alternative text editor
> - [nano](https://git.savannah.gnu.org/cgit/nano.git)

# Base configuration
Our installation have all elemental things, we can continue to configure.
1. `mkdir -p /home/$USER/.config/sway`
2. `cp /etc/sway/config /home/$USER/.config/sway`
3. `vim /home/$USER/.config/sway`

## Set default tools
Before starting Sway, we need to adjust the config file for Sway and select the default choices of tools installed at the beginning.
> Good tip
> - `exec` This command is handy. I recommend understanding `exec` because this command is frequently used in the config files.
### Default terminal 
```
set $term kitty
```

### Default menu (launcher)
```
set $menu exec wofi --show drun
```
You can save and close config file.

### Default display
That part is a little bit tricky, because you need to manually find out display.

#### Get information about display
```
swaymsg -t get_outputs
```
![obrazek](https://user-images.githubusercontent.com/61845673/212125418-4a474680-d896-471d-ad21-77e70ea896f3.png)

#### Config display
In my case display is `Virtual-1`, so I need edit my Sway config by following way:
 1. `vim /home/$USER/.config/sway`
 2. `output Virtual-1 resolution 1920.1080 position 0,0`
