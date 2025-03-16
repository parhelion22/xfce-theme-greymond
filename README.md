# Greymond theme

![Screenshot](https://github.com/parhelion22/xfce-theme-greymond/blob/main/Screenshot.png)

GTK theme aiming to provide a consistent and classic look for GTK 2, GTK 3, and GTK 4 based on the classic "Raleigh" theme.

The GTK 2 part uses the built-in "Raleigh" theme, but explicitly declares all of its colors to facilitate color changes (see "./Greymond/gtk-2.0/gtkrc"). The GTK 3 part was originally based on [raleigh-reloaded](https://github.com/vlastavesely/raleigh-reloaded) but has been modified in order to be more consistent to the GTK 2 theme. The GTK 4 is mostly based on the GTK 3 part, but is work-in-progress.

This project also includes a theme for the Xfce Window Manager (xfwm4), which is based on the "Redmond" theme, a theme for the Xfce notification system (xfce-notify-4.0), and a theme for the LightDM display manager (lightdm-gtk-greeter).

Developed on Arch-based [Manjaro Linux](https://manjaro.org/) running the [Xfce desktop environment](https://www.xfce.org/).

# Installation

Installation differs depending on whether the theme should only be available to the current user or whether it should be available system-wide (for example in order to use it as a theme for the LightDM display manager). For use by the current user, simply copy the directory "Greymond" to you theme directory, for example "\~/.themes/" or "\~/.local/share/themes/". For system-wide use, copy the directory "Greymond" to "/usr/share/themes/" (root privileges required).

## Applying the theme

The following steps can be applied as desired and independently of each other. It is assumed that an Arch-based Linux distribution is used with the Xfce desktop environment. The procedure in other distributions and desktop environments may varry to a greater or lesser extent.

### GTK Application Style

In order for GTK-based applications to use the theme, simply select one of its color variants (e.g. "Greymond Concrete") within "Appearance" settings (xfce4-appearance-settings), tab "Style".

### QT Application Style

One way for QT-based applications to use the theme is by using the "QGtkStyle" theme engine, which renders the QT user interface by using the currently selected GTK 2 theme.

For this to work you have to make sure that the QT 5 and QT 6 configuration tools ("qt5ct", "qt6ct") are installed from the repositories. Also required are the packages "[qt5-styleplugins](https://aur.archlinux.org/packages/qt5-styleplugins)" and "[qt6gtk2](https://aur.archlinux.org/packages/qt6gtk2)" from the AUR, which contain the "QGtkStyle" for QT 5 and QT 6, respectively. After installed, set the environment variable "QT_QPA_PLATFORMTHEME" to "qt5ct", for example by adding "export QT_QPA_PLATFORMTHEME="qt5ct"" to "\~/.profile". After that, select "gtk2" within the "QT 5 Configuration Tool" (qt5ct), tab "Appearance", Combobox "Style", and select "qt6gtk2" under "QT 6 Configuration Tool" (qt5ct), tab "Appearance", Combobox "Style".

### Xfce Window Manager

In order for the Xfce Window Manager (xfwm4) to use the theme, simply select "Greymond" within "Window Manager" settings (xfwm4-settings), tab "Style". The theme will automatically follow the colors of this or any other GTK 3 theme.

### Xfce Notifications System

In order for the Xfce notification system to use the theme, simply select "Greymond" within "Notifications" settings (xfce4-notifyd-config), tab "Appearance", Combobox "Theme". The theme will use the colors of the color variant selected as application style.

### Icon Theme

A suitable classic icon theme is "[Hedera](https://www.gnome-look.org/p/1207800)". Install it (e.g. by copying the directory "Hedera" to "/usr/share/icons/", root privileges needed) and select it under "Appearance" settings (xfce4-appearance-settings), tab "Icons".

### Mouse Cursor Theme

A suitable classic mouse cursor theme is "DMZ (White)", which is available as "xcursor-vanilla-dmz" from the repositories. Select it under "Mouse and Touchpad" Settings (xfce4-mouse-settings), tab "Theme".

# Color Variants

"Greymond Concrete" can be seen as the default color variant for this theme, but there are a few other familiar color variants. Colors are mostly defined within "./gtk-2.0/gtkrc" and "./gtk-3.0/colors.css" for the GTK 2 and GTK 3 theme, respectively. Basically, all colors can be adjusted by changing the color values within these files.

![Color Variants](https://github.com/parhelion22/xfce-theme-greymond/blob/main/ColorVariants.png)

# License

This project is licensed under the [GNU General Public License v3.0](/LICENSE).