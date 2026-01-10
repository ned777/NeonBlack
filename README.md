# NeonBlack

A dark, tech-inspired GTK/Metacity/Cinnamon theme with teal accents.

**Author:** Ned Nguyen  
**License:** GPL-3.0

## Features
- Pure black (#000000) backgrounds
- Teal (#008080) accents and highlights
- Yellow (#ffff00) focused window borders
- Sharp, angular design (no rounded corners)
- Optimized for Cinnamon/Linux Mint
- Supports GTK 3.0, GTK 3.20, Metacity/Muffin window managers

## Preview

###Screenshots
screenshots/Screenshot.jpeg

## Color Palette

| Element | Color | Hex Code |
|---------|-------|----------|
| Background | Black | #000000 |
| Text | White | #ffffff |
| Focused Border | Yellow | #ffff00 |
| Unfocused Border | Teal | #008080 |
| Accent/Highlight | Bright Teal | #00aaaa |
| UI Elements | Dark Gray | #1a1a1a |
| Disabled Text | Gray | #666666 |

## Installation

### Quick Install
```bash
# Clone the repository
git clone https://github.com/ned777/NeonBlack.git

# Copy to themes directory
cp -r NeonBlack ~/.themes/

# Apply the theme
gsettings set org.cinnamon.desktop.interface gtk-theme "NeonBlack"
gsettings set org.cinnamon.desktop.wm.preferences theme "NeonBlack"
gsettings set org.cinnamon.theme name "NeonBlack"
```

For detailed installation instructions, see [INSTALL.md](INSTALL.md).

## Compatibility

- **Desktop Environment:** Cinnamon 3.0+, MATE, GNOME (partial)
- **GTK Version:** GTK 3.0, GTK 3.20+
- **Window Manager:** Metacity, Muffin, Marco
- **Tested on:** Linux Mint 21.x, Linux Mint 22.x

## Components

This theme includes:
- **GTK Theme** - Controls, buttons, menus, and application widgets
- **Window Manager Theme** - Window borders and decorations (Metacity/Muffin)
- **Cinnamon Theme** - Desktop panel, applets, and system UI

## Customization

All colors can be customized by editing:
- `gtk-3.0/gtk.css` - GTK styling
- `gtk-3.20/gtk.css` - GTK 3.20+ styling  
- `metacity-1/metacity-theme-3.xml` - Window borders
- `cinnamon/cinnamon.css` - Cinnamon desktop

See [INSTALL.md](INSTALL.md) for detailed customization instructions.

## Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

### To Do
- [ ] Add GTK 2.0 support
- [ ] Create icon theme variant
- [ ] Add more color variants (purple, orange, etc.)
- [ ] Improve Flatpak app compatibility
- [ ] Add more screenshots

## Credits

Created and maintained by **Ned Nguyen**

Inspired by cyberpunk aesthetics and terminal themes.

## License

This project is licensed under the GPL-3.0 License - see the [LICENSE](LICENSE) file for details.

## Support

If you find this theme useful, consider:
- ⭐ Starring the repository
- 🐛 Reporting bugs or issues
- 🎨 Suggesting improvements
- 📣 Sharing with others

---

**Repository:** [https://github.com/ned777/NeonBlack](https://github.com/ned777/NeonBlack)  
**Author:** Ned Nguyen  
**Version:** 1.0.0  
**Last Updated:** January 2026
