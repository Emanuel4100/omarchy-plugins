# Omarchy plugins

All of my [Omarchy 4](https://omarchy.org) shell plugins in one place. Each one
lives in its own repo and is pulled in here as a git submodule.

| Plugin | Id | Kind | What it does | Install |
|---|---|---|---|---|
| [Gnomarchy](https://github.com/Emanuel4100/gnomarchy) | `emanuel.gnomarchy` | panel, service | GNOME Dash-style auto-hide dock with pinned/running apps, dynamic workspaces, and a one-toggle GNOME mode | `omarchy plugin add https://github.com/Emanuel4100/gnomarchy.git --enable` |
| [Boot Into](https://github.com/Emanuel4100/omarchy-boot-into) | `emanuel.boot-into` | service | Reboot once into Windows, another distro, or firmware setup from the System menu (UEFI `BootNext`) | `omarchy plugin add https://github.com/Emanuel4100/omarchy-boot-into.git` |
| [Dotstate](https://github.com/Emanuel4100/omarchy-dotstate-widget) | `emanuel.dotstate` | bar-widget | Dotfiles sync status against the dotstate remote, with a Sync Now action | `omarchy plugin add https://github.com/Emanuel4100/omarchy-dotstate-widget.git --enable` |
| [Hide Top Bar](https://github.com/Emanuel4100/omarchy-hide-top-bar) | `emanuel.hide-top-bar` | service | Auto-hides the bar and reveals it when the pointer nears its edge | `omarchy plugin add https://github.com/Emanuel4100/omarchy-hide-top-bar.git --enable` |
| [HyperX Mouse Battery](https://github.com/Emanuel4100/omarchy-hyperx-battery) | `emanuel.hyperx-battery` | bar-widget | Battery %, charging state, and low-battery alert for the HyperX Pulsefire Haste 2 Wireless | `omarchy plugin add https://github.com/Emanuel4100/omarchy-hyperx-battery.git`, then run its `install.sh` |
| [Power Mode](https://github.com/Emanuel4100/omarchy-power-mode) | `power-mode` | panel | Switch refresh rate, resolution, scale, and power profile between AC and battery, with presets in the launcher | `omarchy plugin add https://github.com/Emanuel4100/omarchy-power-mode.git --enable` |

Some plugins also ship a CLI in `bin/` to symlink into `~/.local/bin`, or menu
entries in `extras/` to paste into `~/.config/omarchy/extensions/omarchy-menu.jsonc`.
Each plugin's README has the details.

## This repo

Install plugins with `omarchy plugin add` (above), not from this checkout.
It's for browsing everything together:

```bash
git clone --recursive https://github.com/Emanuel4100/omarchy-plugins.git
```

Update every submodule to its latest commit:

```bash
git submodule update --remote --merge
git commit -am "Bump plugins"
```

## License

The index is MIT. Each plugin has its own license (see its repo).
