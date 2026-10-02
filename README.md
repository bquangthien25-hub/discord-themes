# macOS Modern

A Liquid Glass–inspired Discord theme that makes Discord look and feel like a native macOS app. Panels are translucent and tinted by the wallpaper behind them. The window controls are macOS traffic lights. Channels, servers, messages and buttons react to the pointer with smooth, springy motion.

The wallpaper is embedded in the theme file, so the theme never loads images from an outside server.

<img width="2556" height="1529" alt="macOS Modern theme preview" src="https://github.com/user-attachments/assets/deeda668-4dfd-4763-880d-0af87b3c66d3" />

## Features

### Liquid glass surfaces
- Server list, channel sidebar, member list, user panel and channel header all use translucent, wallpaper-tinted glass with a strong blur.
- Each panel has a light sheen across its surface and a thin bright edge along the top.
- Menus, popouts, profile cards and the message composer share the same glass style.
- Text stays readable on top of the glass: channel names, messages and typed text are always light.

### macOS window controls
- Discord's window buttons become 12px traffic lights in macOS order: close, minimize, maximize.
- Hovering over the group shows the `×` `−` `+` symbols.
- The lights turn grey when the window is not focused.
- The back and forward arrows sit right next to the traffic lights.

### Motion and hover effects
- **Channels and voice users**: slide slightly and show a glossy glass background on hover. The selected channel becomes an accent-tinted glass pill.
- **Server icons**: lift with a spring and a soft glow, and press in when clicked.
- **Messages**: hovered rows get a rounded glass background and the avatar grows slightly. The message action bar becomes a floating glass capsule.
- **Buttons**: lift on hover and press in on click.
- **Menus**: right-click menus and popouts scale in smoothly, and the highlighted item is blue like on macOS.

### Accessibility
- If your system has reduced motion turned on, animations and transitions are switched off.
- Keyboard focus shows a visible outline.

## Installation

### Vencord / Vesktop

1. Download [`macOS-Modern.theme.css`](./macOS-Modern.theme.css).
2. Open **User Settings → Vencord → Themes** and click **Open Themes Folder**.
3. Put the file in that folder and enable **macOS Modern**.

> Vesktop installed through Flatpak keeps its themes in `~/.var/app/dev.vencord.Vesktop/config/vesktop/themes/`.

### BetterDiscord

1. Download [`macOS-Modern.theme.css`](./macOS-Modern.theme.css).
2. Open **User Settings → Themes** and click **Open Themes Folder**.
3. Put the file in that folder and turn the theme on.

### Keeping it up to date while editing

If you are editing the theme from a clone of this repo, symlink the file into the themes folder instead of copying it. Discord then reloads the theme every time you save:

```bash
ln -sf "$PWD/macOS-Modern.theme.css" ~/.var/app/dev.vencord.Vesktop/config/vesktop/themes/macOS-Modern.theme.css
```

## Customization

Every value below is a CSS variable in the `:root` block at the top of `macOS-Modern.theme.css`.

| Variable | What it controls |
| --- | --- |
| `--wallpaper` | Background image. You can use any image URL or a `data:` URI. |
| `--accent-color` | Selected channel, focus rings, highlighted menu items and primary buttons. |
| `--glass-bg` / `--glass-bg-strong` | Tint and opacity of the glass panels. Lower the alpha for clearer glass. |
| `--glass-blur` / `--glass-saturate` | How strongly the glass blurs the wallpaper and boosts its colors. |
| `--glass-sheen` | The light reflection drawn across the glass surfaces. |
| `--macos-red` / `--macos-yellow` / `--macos-green` | Traffic light colors. |
| `--panel-radius` / `--control-radius` | Corner rounding for panels and inputs. |

Dark mode overrides some of these in the `:root[data-theme="dark"]` block, so change them there as well.

## Compatibility

The theme is built for current Vencord, Vesktop and BetterDiscord builds. It finds Discord's elements by partial class names such as `[class*="sidebar_"]`, which keeps working through most Discord updates. Even so, a major Discord UI change can break individual parts of the theme. If something looks wrong, please open an issue with a screenshot.
