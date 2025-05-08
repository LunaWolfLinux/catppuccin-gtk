# About

This is a fork of discontinued catppuccin gtk theme, that are based a [Colloid](https://github.com/vinceliuice/Colloid-gtk-theme) theme made by [Vinceliuice](https://github.com/vinceliuice)

# Usage 

### Requirements
- GTK '>=3.20'
- `gnome-themes-extra`

# Installation

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
flatpak override --user --filesystem=$HOME/.themes:ro
```

2. To give your Flatpak applications access to the `~/.config/gtk-3.0` and `~/.config/gtk-4.0` configuration directories run:

```bash
flatpak override --user --filesystem=xdg-config/gtk-3.0:ro
flatpak override --user --filesystem=xdg-config/gtk-4.0:ro
```

# Manual Building
Run the following command in the terminal
```
python build.py
```
> Tip: `python build.py` allows (and requires *) the following options:
```
Compulsory field *      Specify color variant(s) [mocha|frappe|macchiato|latte|all]
-d, --dest DIR *        Specify destination directory
-n, --name NAME *       Specify theme name
-a, --accent VARIANT *  Specify theme color variant(s) [rosewater|flamingo|pink|mauve|red|maroon|peach|yellow|green|teal|sky|
                        sapphire|blue|lavender|all]
-s, --size VARIANT      Specify size variant [standard|compact] (Default: standard variant)
-l, --link              Link installed gtk-4.0 theme to config folder for all libadwaita app use this theme
--zip                   Zips up the finally produced themes.
--tweaks                Specify versions for tweaks [black|rimless|normal|float]
                        1. black:    Blackness color version
                        2. rimless:  Remove the 1px border about windows and menus
                        3. normal:   Normal windows button style (titlebuttons: max/min/close)
                        4. float:    Floating gnome-shell panel style
-h, --help              Show help
```
```
