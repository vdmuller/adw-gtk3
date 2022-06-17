Adw-gtk3 allows you to change the colors the same way as libadwaita. For example if you just want to change the accent colors:

1. Create or open `~/.config/gtk-3.0/gtk.css`
2. Add:
```css
/* Add an accent color from the theme's palette. Replace @green_4 with any hex color value, or select a color from _palette.scss */
@define-color accent_color @green_4;
@define-color accent_bg_color @green_4;
```
3. Save the file. This does not change seamlessly, so you'll have to close any open application to see the changes.

If you want to use the same colors in libadwaita/gtk4 simply copy or symlink `gtk.css` to `~/.config/gtk-4.0/gtk.css`

Flatpak apps may need a permission setting:
```bash
sudo flatpak override --filesystem=xdg-config/gtk-3.0 && sudo flatpak override --filesystem=xdg-config/gtk-4.0
```

Named colors that you can change: https://gnome.pages.gitlab.gnome.org/libadwaita/doc/1.1/named-colors.html

## Color themes for adw-gtk3 and libadwaita

TODO
