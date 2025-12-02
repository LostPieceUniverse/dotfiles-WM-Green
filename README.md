# Welcome to my Froggo setup :frog:

My personal configuration files for my Windowmanager on EndeavorOS.

![Desktop Setup](./Image.png)

## Contents

This repository includes configuration files for:

- **Sway** - Wayland compositor with custom keybindings and auto-start applications
- **Waybar** - Status bar for Wayland
- **Wofi** - Application launcher

## Installation

Clone this repository:

```bash
git clone https://github.com/LostPieceUniverse/dotfiles-WM-Green.git
cd dotfiles-WM-Green/
```

You can either copy the configuration files or create symlinks. Symlinks are recommended as they allow you to keep your configurations in sync with this repository.

### Option 1: Using Symlinks

```bash
ln -sf "$PWD/sway" ~/.config/sway
ln -sf "$PWD/waybar" ~/.config/waybar
ln -sf "$PWD/wofi" ~/.config/wofi
```

### Option 2: Copying Files

```bash
cp -r sway ~/.config/
cp -r waybar ~/.config/
cp -r wofi ~/.config/
```

## Requirements

Make sure you have the following packages installed:

```bash
sudo pacman -S sway waybar wofi fish alacritty swaylock swayidle grim brightnessctl
```

Additional dependencies for the Sway configuration because of autostart:
- **Firefox** - Default browser (on workspace 1)
- **Signal** (Flatpak) - Messaging app (on workspace 10)
- **Bitwarden** (Flatpak) - Password manager (on workspace 3)
- **Chromium** (Flatpak) - Browser (on workspace 9)

## Configuration Highlights

### Sway
- Super key (Mod4) as modifier
- Vim-style navigation (hjkl)
- Three keyboard layouts: US, DE, FR (switch with Mod+Space)
- Auto-lock after 15 minutes
- Custom wallpaper support
- Volume and brightness controls
- Screenshot support with grim

### Key Bindings
- `Mod+Return` - Open terminal (Alacritty with Fish)
- `Mod+d` - Launch application menu (Wofi)
- `Mod+q` - Close window
- `Mod+Escape` - Lock screen
- `Print` - Take screenshot

## Usage

After installing the configuration files, restart Sway or reload the configuration:

```bash
sway reload
```

For Fish shell:
```bash
source ~/.config/fish/config.fish
```


