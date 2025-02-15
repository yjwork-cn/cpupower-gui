cpupower-gui
--------------------
[![latest packaged version(s)](https://repology.org/badge/latest-versions/cpupower-gui.svg)](https://repology.org/project/cpupower-gui/versions)

This program is designed to allow you to change the frequency limits of your cpu and its governor. The application is similar in functionality to `cpupower`.

# Screenshots
The theme used is [Arc-Darker](https://github.com/horst3180/arc-theme).
<img src="screenshots/screen_cpu0.png" alt="Default view" width="844"/>
<img src="screenshots/screen_cpu1_freq.png" alt="Change frequencies" width="420"/>  <img src="screenshots/screen_cpu2_governor.png" alt="Change governors" width="420"/>

# Packages
Cpupower-gui is available on the official repositories for a few distributions.

[![Packaging status](https://repology.org/badge/vertical-allrepos/cpupower-gui.svg)](https://repology.org/metapackage/cpupower-gui/versions)

Prebuilt binary packages for Arch, Debian/Rasbian, Fedora, and Ubuntu are available on [openSUSE Build Service](https://software.opensuse.org/download.html?project=home%3Aerigas%3Acpupower-gui&package=cpupower-gui)

## Repositories:

### Arch Linux and derivatives
Packages exist in AUR as [`cpupower-gui`](https://aur.archlinux.org/packages/cpupower-gui/) ([`cpupower-gui-git`](https://aur.archlinux.org/packages/cpupower-gui-git/)), built from this repo.

### blackPanther OS 
To install `cpupower-gui` run `updating repos` to update the repositories and install by running `installing cpupower-gui`.


# Manual Installation
This package uses the [Meson build system](https://mesonbuild.com/) for build configuration and [Ninja](https://ninja-build.org/) as the backend build system.

## Clone the repository

```bash
git clone https://github.com/vagnum08/cpupower-gui.git
cd cpupower-gui
```

## Install build dependencies
The main build depencies are `meson (>=0.50.0)`, `ninja`, `glib2.0`, and `pkg-config`.

To install them,

- On Arch and derivatives: `pacman -Sy pkg-config meson`
- On blackPanther OS and derivatives: (TBD)
- On Debian and derivatives: `apt update && apt install  meson ninja-build, pkg-config, libglib2.0-bin, libglib2.0-dev`
- On Fedora: (TBD)

Optionally (for meson check) the following programs are needed:  `desktop-file-validate`, `appstream-util`, `glib-compile-schemas`.

To install them,

- On Arch and derivatives: `pacman -Sy desktop-file-utils appstream-glib`
- On blackPanther OS and derivatives: (TBD)
- On Debian and derivatives: `apt update && apt install appstream-util desktop-file-utils`
- On Fedora: (TBD)

## Build cpupower-gui
```bash
meson build
ninja -C build
```

## Install
To uninstall run `ninja -C build install`

## Uninstall

To uninstall run `ninja -C build uninstall`.

# Runtime Dependencies
## Arch Linux and derivatives
`python` `gtk3` `hicolor-icon-theme` `polkit` `python-dbus` `python-gobject`

## blackPanther OS and derivatives
`python3`, `gtk3`, `hicolor-icon-theme`, `polkit`, `python3-dbus`, `python3-gobject3`

## Debian and derivatives
`libgtk-3-0` `gir1.2-gtk-3.0` `hicolor-icon-theme` `policykit-1` `python3-dbus` `python3-gi`

Suggested for authentication dialogue: `policykit-1-gnome` or `mate-polkit` or `lxpolkit`
