# About

This is a fork of discontinued catppuccin gtk theme, that are based a [Colloid](https://github.com/vinceliuice/Colloid-gtk-theme) theme made by [Vinceliuice](https://github.com/vinceliuice)

# Usage 

### Requirements
- GTK '>=3.20'
- `gnome-themes-extra`

#Installation

1. Download theme zip from [releases](https://github.com/VanillaDaFur/catppuccin-gtk/releases/)
2. Extract the archive to a ~/.themes folder
3. Select the downloaded theme via your desktop specific tweak application (**gnome-tweaks** on GNOME)

### For GTK 4 applications
To theme GTK 4 applications you have to manually symlink the `~/.config/gtk-4.0` to the themes folder. Use the following commands

```bash
mkdir -p "${HOME}/.config/gtk-4.0"
ln -sf "${THEME_DIR}/gtk-4.0/assets" "${HOME}/.config/gtk-4.0/assets"
ln -sf "${THEME_DIR}/gtk-4.0/gtk.css" "${HOME}/.config/gtk-4.0/gtk.css"
ln -sf "${THEME_DIR}/gtk-4.0/gtk-dark.css" "${HOME}/.config/gtk-4.0/gtk-dark.css"
```

### For Flatpak applications

1. To give your Flatpak applications access to your themes folder run:

```bash
flatpak override --filesystem=$HOME/.themes:ro
```

2. To give your Flatpak applications access to the `~/.config/gtk-3.0` and `~/.config/gtk-4.0` configuration directories run:

```bash
flatpak override --user --filesystem=xdg-config/gtk-3.0:ro
flatpak override --user --filesystem=xdg-config/gtk-4.0:ro
```

