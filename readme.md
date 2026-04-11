<img src="https://raw.githubusercontent.com/cybrcore/cybrcore/refs/heads/main/assets/repo-banners/cybr-broot-banner-top.png"/>

# Showcase
<img src="https://raw.githubusercontent.com/cybrcore/cybrcore/refs/heads/main/assets/showcase/cybr-broot.png"/>

# Steps
## 0. Before you start
- Make sure [Geist Mono Nerd Font](https://www.nerdfonts.com/font-downloads) is installed, you can do that from terminal with:
```bash
curl -L https://github.com/ryanoasis/nerd-fonts/releases/latest/download/GeistMono.zip -o GeistMono.zip
mkdir -p ~/.local/share/fonts
unzip GeistMono.zip -d ~/.local/share/fonts/GeistMono
fc-cache -fv
```
- Make sure kitty is installed: `sudo pacman -S kitty` and [cybrcore theme](https://github.com/cybrcore/cybr-kitty) is applied
- Make sure broot is installed: `sudo pacman -S broot`
- See [Installation Guide](https://github.com/cybrcore/cybrdots/blob/main/INSTALL.md) if you're coming from [cybr-hyprland](https://github.com/cybrcore/cybr-hyprland) and haven't set up prerequisites yet
- [broot Github repo](https://github.com/Canop/broot)

## 1. Create theme folder and file
```sh
mkdir -p ~/.config/broot/skins
$EDITOR ~/.config/broot/skins/cybrcore.hjson
```
## 2. Insert [cybr-bat theme](cybrcore.hjson)
## 3. Apply theme
```sh
# Open config
$EDITOR ~/.config/broot/config.hjson

# Enable True Colors and Icons
true_colors: true
icon_theme: nerdfont

# Add skin under luma: [dark] section
file: skins/cybrcore.hjson

# It should look like this:
{
luma: [
	dark
	unknown
]
//file: foo.hjson
//file: bar.hjson
file: skins/cybrcore.hjson
}
```
## 4. Restart terminal
```sh
pkill $TERM
```