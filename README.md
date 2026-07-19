<div align="center">

# hyprland-wallpapers

[![Type](https://img.shields.io/badge/type-wallpaper%20pack-8b5cf6)](#whats-inside)
[![WM](https://img.shields.io/badge/wm-Hyprland-00B4D8?logo=archlinux&logoColor=white)](https://hyprland.org)
[![License](https://img.shields.io/badge/license-MIT-8b5cf6)](#license)

</div>

A curated wallpaper pack for a Hyprland desktop. It mixes still images
(photography, renders, AI-generated scenes) with short video loops for
animated backgrounds, so you can point `hyprpaper` or a video wallpaper setup
at the folder and switch freely.

## What's inside

The repo is flat media — no code, no build step:

- **Stills** — `*.png` / `*.jpg` (landscapes, wave/ mountain renders, AI
  scenes like *Niri pool blue*, *a blue circle with a wave in the middle*).
- **Loops** — `*.mp4` (e.g. `2.mp4`, `3.mp4`, *Thriller (low quality).mp4*) for
  animated wallpaper.

Pick by mood: calm naturals (*a mountain with a lake in the background*),
abstract renders (*a close up of a circuit board*), or playful AI cartoons
(*a cartoon of a cat on a balcony*).

## Using it

With [`hyprpaper`](https://github.com/hyprwm/hyprpaper):

```ini
# hyprpaper.conf
preload = /path/to/hyprland-wallpapers/Niri pool blue.png
wallpaper = eDP-1,/path/to/hyprland-wallpapers/Niri pool blue.png
```

Or cycle through the folder:

```bash
for img in /path/to/hyprland-wallpapers/*.png; do
  hyprctl hyprpaper wallpaper "eDP-1,$img"
done
```

For the `.mp4` loops, use a video-wallpaper helper (e.g. `mpvpaper` /
`hydrapaper`) pointed at the file.

## Layout

```
hyprland-wallpapers/
├── *.png  *.jpg     # still wallpapers
└── *.mp4            # animated loops
```

## License

MIT — use freely; attribute the source if a particular image requires it.
