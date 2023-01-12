# Sway guide
I decided to create guide how jump from KDE to Sway and more CLI environment. I hope that guide help other people with Sway useage.

## Why Sway?
I found some benefitcs of Sway - Window Managers in gerneral compare to Desktop Environment:
- Lower hardware usage: CPU, RAM, GPU
- Potential to get better battery life on laptop.
- Much better gaming expericnes - fps boost, frametimes stability

- [Base](#base)
  - [Sway Installation](#sway-installation)
  - [Tools](#tools)
  
# Base
You need to satisfy the following steps to get Sway working and to be ready for post-install configuration.

## Sway-Installation
You need install following packages
```
sudo pacman -S --needed sway swaybg swayidle swayimg swaylock
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
