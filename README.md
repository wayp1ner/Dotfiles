# waypiner's Linux dotfiles (based on **[stdrice's dotfiles](https://github.com/stdrice/dotfiles)**)

- [Starring](#starring)
- [Installation](#installation)
- [Keybindings](#keybindings)

# Starring
<img src="https://files.catbox.moe/k9a6bs.png" align="right" width="400px">

- **[Sway ⚽](https://swaywm.org)**: Window Manager/Compositor
- **[Foot ❤️](https://codeberg.org/dnkl/foot)**: Terminal
- **[LibreWolf 🦊](https://librewolf.net)**: Browser
- **[Neovim 📓](https://neovim.io/)**: Text Editor
- **[Ranger](https://ranger.github.io) and [Nemo](https://github.com/linuxmint/nemo)**: File Manager
- **[ncmpcpp](https://github.com/ncmpcpp/ncmpcpp)**: Music Player
- **[calcurse](https://www.calcurse.org)**: Calendar
- **[Waterfall](https://github.com/crambaud/waterfall)**: CSS/theme browser
- **[btop](https://github.com/aristocratos/btop)**: System monitor

# Installation
1. Install all dependencies
  I use rebos because make install dependencies easier and I use yay

  Install yay
```
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si
cd ..
rm -rf yay
```
  Install rustup & cargo
```
sudo pacman -S rustup cargo base-devel
```
  Install rebos
```
cargo install rebos
```
  Clone my rebos config and install my rebos config
```
git clone https://github.com/waypiner/Rebos-arch ~/.config/rebos
rebos setup
rebos config init
rebos gen commit "initial"
rebos gen current build
```

2. Clone this repo
```
git clone https://github.com/waypiner/Dotfiles
```
3. Backup all your files
4. Copy all files in `dotfiles` and paste to your `$HOME` folder
```
cp -rfT Dotfiles/ $HOME/
```
5. Other setup
```
chsh -s /usr/bin/zsh
systemctl --user enable pipewire pipewire-pulse wireplumber
```

# Keybindings
These are the basic keybinds. Read through the `sway/general/keybindings.conf` file for more keybinds.
> Note: Mod = Windows key

| Keys                                              | Function                          |
| :------------------------------------------------ | :-------------------------------- |
| `Mod + Enter`                                     | Launch terminal (foot)            |
| `Mod + Q`                                         | Close window                      |
| `Mod + Shift + E`                                 | Reload config files               |
| `Mod + Space`                                     | Open launcher (rofi)              |
| `Mod + Shift + C`                                 | Open powermenu                    |
| `Mod + Delete`                                    | Screenshot menu                   |
| `Mod + S/W/E`                                     | Stacking/Tabbed/Tile              |
| `Mod + F`                                         | Toggle Fullscreen                 |
| `Mod + B/V`                                       | Split Horizontal/Vertical         |
| `Mod + R`                                         | Resize mode                       |
| `Mod + Shift + Space`                             | Toggle Floating                   |
| `Mod + H/J/K/L or Left/Down/Up/Right`             | Change Focus                      |
| `Mod + Shift + H/J/K/L or Left/Down/Up/Right`     | Move window                       |
| `Mod + Alt + L`                                   | Locksrceen                        |
