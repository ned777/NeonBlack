# CyberTeal Theme - Installation Instructions

## Theme Specifications
- **Background:** #000000 (pure black)
- **Focused window border:** Yellow (#ffff00)
- **Unfocused window border:** Teal (#008080)
- **Accent color:** Teal (#008080, #00aaaa for highlights)
- **Border width:** 1px
- **Border radius:** 0 (sharp corners, no rounding)
- **Supports:** GTK 3.0, GTK 3.20, Metacity/Muffin, Cinnamon

## Requirements
- Linux Mint (Cinnamon edition) or any GTK-based desktop
- Cinnamon 3.0+ (for full Cinnamon theme support)
- Metacity or Muffin window manager

## Installation

### Method 1: User Installation (Recommended)
1. Create a themes directory in your home folder if it doesn't exist:
   ```bash
   mkdir -p ~/.themes
   ```

2. Copy the CyberTeal folder to your themes directory:
   ```bash
   cp -r CyberTeal ~/.themes/
   ```

3. Set proper permissions:
   ```bash
   chmod -R 755 ~/.themes/CyberTeal
   ```

### Method 2: System-wide Installation (requires root)
1. Copy the CyberTeal folder to the system themes directory:
   ```bash
   sudo cp -r CyberTeal /usr/share/themes/
   ```

2. Set proper permissions:
   ```bash
   sudo chmod -R 755 /usr/share/themes/CyberTeal
   ```

## Applying the Theme

### Using System Settings (GUI):
1. Open **Menu → System Settings**
2. Click on **Themes**
3. Under **Window borders** select "CyberTeal"
4. Under **Controls** select "CyberTeal"
5. Under **Desktop** select "CyberTeal" (for Cinnamon desktop styling)

### Using Command Line:
```bash
# Apply GTK theme (controls, menus, buttons)
gsettings set org.cinnamon.desktop.interface gtk-theme "CyberTeal"

# Apply window manager theme (window borders)
gsettings set org.cinnamon.desktop.wm.preferences theme "CyberTeal"

# Apply Cinnamon theme (panel, applets)
gsettings set org.cinnamon.theme name "CyberTeal"
```

### For Metacity Window Manager (if not using Cinnamon):
```bash
gsettings set org.gnome.desktop.wm.preferences theme "CyberTeal"
```

## Reloading the Theme

After installation or making changes:

1. **Restart Cinnamon:**
   - Press `Alt+F2`
   - Type `r` and press Enter
   
   OR
   
   ```bash
   cinnamon --replace &
   ```

2. **Reload window manager theme:**
   ```bash
   killall -HUP muffin
   ```

3. **If all else fails, log out and log back in**

## Troubleshooting

### Theme doesn't appear in the list:
- Verify the folder structure is correct (see below)
- Check that `index.theme` file exists
- Log out and log back in
- Run: `gtk-update-icon-cache ~/.themes/CyberTeal/` (if you have icon theme components)

### Window borders don't change:
- Make sure you're applying the theme under "Window borders" not just "Controls"
- Try: `killall -HUP muffin` or `cinnamon --replace &`
- Verify you have both metacity-theme-2.xml and metacity-theme-3.xml files

### Some applications don't use the theme:
- Some apps (Firefox, Chrome, Electron apps) use their own themes
- Flatpak apps need: `sudo flatpak override --filesystem=~/.themes`
- Some GTK2 apps won't work with GTK3-only themes

## Required Folder Structure

```
CyberTeal/
├── index.theme          # Theme metadata (REQUIRED)
├── gtk-3.0/
│   └── gtk.css         # GTK 3.0 styling
├── gtk-3.20/
│   └── gtk.css         # GTK 3.20+ styling
├── metacity-1/
│   ├── metacity-theme-2.xml  # Window borders (Metacity 2)
│   └── metacity-theme-3.xml  # Window borders (Metacity 3/Muffin)
└── cinnamon/
    ├── cinnamon.css    # Cinnamon desktop styling
    └── thumbnail.png   # Theme preview (optional)
```

## Customization

You can modify the colors by editing these files:

### GTK Theme (buttons, menus, widgets):
- `CyberTeal/gtk-3.0/gtk.css`
- `CyberTeal/gtk-3.20/gtk.css`

### Window Borders:
- `CyberTeal/metacity-1/metacity-theme-3.xml`
- Look for color constants at the top:
  ```xml
  <constant name="C_border_focused" value="#ffff00" />
  <constant name="C_border_unfocused" value="#008080" />
  ```

### Cinnamon Desktop (panel, applets):
- `CyberTeal/cinnamon/cinnamon.css`

### Main Colors Used:
| Element | Color | Hex Code |
|---------|-------|----------|
| Background | Black | #000000 |
| Text | White | #ffffff |
| Focused border | Yellow | #ffff00 |
| Unfocused border | Teal | #008080 |
| Accent/Highlight | Bright Teal | #00aaaa |
| UI elements | Dark Gray | #1a1a1a |
| Borders | Gray | #333333 |
| Disabled text | Gray | #666666 |

## Uninstallation

### User Installation:
```bash
rm -rf ~/.themes/CyberTeal
```

### System Installation:
```bash
sudo rm -rf /usr/share/themes/CyberTeal
```

Then select a different theme in System Settings.

## Support

If you encounter issues:
1. Check the GitHub Issues page
2. Verify your Cinnamon/GTK version: `cinnamon --version` and `gtk-launch --version`
3. Check theme installation location and permissions
4. Review error logs: `~/.xsession-errors`

## License

This theme is released under GPL-3.0 License.
