Adw-gtk3 allows you to change the colors the same way as libadwaita. For example if you just want to change the accent colors:

1. Create or open `~/.config/gtk-3.0/gtk.css`
2. Add:
```css
/* Add an accent color from the theme's palette. Replace @green_4 with any hex color value, or select a color from _palette.scss */
@define-color accent_color @green_4;
@define-color accent_bg_color @green_4;
```
3. Save the file. This does not change seamlessly, so you'll have to close and re-open any apps.

If you want to use the same colors in libadwaita/gtk4 simply copy or symlink `gtk.css` to `~/.config/gtk-4.0/gtk.css` or vice versa.

Flatpak apps may need a permission setting:
```bash
sudo flatpak override --filesystem=xdg-config/gtk-3.0 && sudo flatpak override --filesystem=xdg-config/gtk-4.0
```

Named colors that you can change: https://gnome.pages.gitlab.gnome.org/libadwaita/doc/1.1/named-colors.html

## Color themes for adw-gtk3 and libadwaita

Note: GTK-3 is CPU rendered while libadwaita is GPU rendered. To get better CPU performance adw-gtk3 is not using too many transparent colors like libadwaita. Because of that reason you may notice some minor color mismatches between GTK-3 and 4 in the color themes. (It should still be close enough.)

Here are some premade color themes that you can use. Use light themes with `adw-gtk3` and dark themes with `adw-gtk3-dark` enabled.

TODO

| Color theme | Screenshot |
|:------------|:-----------|
| placeholder | placeholder |
