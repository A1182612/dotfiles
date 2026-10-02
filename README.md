# Arch Linux XFCE Dotfiles

My customized Arch Linux desktop setup featuring XFCE4, Openbox, Rofi, Tint2, Picom, and Btop.

---

## 🎨 Overview & Features
- **OS:** Arch Linux
- **Desktop Environment / Window Manager:** XFCE4 / Openbox
- **Launcher:** Rofi
- **Panel:** Tint2
- **Compositor:** Picom
- **System Monitor:** Btop
- **⚡ Performance Tested:** Runs extremely well on modest specs (tested on an Intel i3-5005U with 6GB RAM).

---

## 📦 Software & Packages
- `pkglist.txt` — Explicitly installed official Arch packages (`pacman`).
- `aurlist.txt` — Installed AUR packages (`yay` / `paru`).

---

## 🚀 How to Install on Your Machine

> ⚠️️ **Warning:** Copying dotfiles directly will overwrite existing configurations in `~/.config/`. Back up your existing configuration folders before proceeding!

### 1. Clone this repository:
```bash
git clone [https://github.com/A1182612/dotfiles.git](https://github.com/A1182612/dotfiles.git) ~/dotfiles
```
### 2. reinstall pachages (Arch linux only!):
```bash
sudo pacman -S --needed - < ~/dotfiles/pkglist.txt
```
For Non-Arch Users:

Do not copy-paste the full pkglist.txt. Standalone apps exist in most distro repositories under identical or similar names. Search for and install them using your package manager:

Ubuntu / Debian / Mint: ```sudo apt install <package-name>```

Fedora: ```sudo dnf install <package-name>```

(Tip: Use apt search <app> or visit https://pkgs.org/  to find the exact package name for your distro).

### 3. Copy configurations to ~/.config/:
Copy only the specific configurations you want to try:

   Optional: Create a quick backup of your current .config folder
  ```bash
  cp -r ~/.config ~/.config-backup
  ```
   Copy configurations
  ```bash
  cp -r ~/dotfiles/xfce4/* ~/.config/xfce4/ 2>/dev/null || true
  cp -r ~/dotfiles/openbox/* ~/.config/openbox/ 2>/dev/null || true
  cp -r ~/dotfiles/rofi/* ~/.config/rofi/ 2>/dev/null || true
  cp -r ~/dotfiles/tint2/* ~/.config/tint2/ 2>/dev/null || true
  cp -r ~/dotfiles/picom/* ~/.config/picom/ 2>/dev/null || true
  ```
   Copy Btop configuration
  ```bash
  mkdir -p ~/.config/btop
  cp ~/dotfiles/btop/btop.conf ~/.config/btop/ 2>/dev/null || true
  ```

### 4. Apply Changes:
After installing the packages and copying the configurations to ~/.config/, log out of your desktop session and log back in.

### ⌨️ Master Keyboard Shortcuts Quick Reference
🚀 Application Launchers & System Utilities
| Shortcut | Action |
| :--- | :--- |
| `Ctrl` + `Alt` + `T` | Open Terminal |
| `Super` + `Space` | Launch Rofi App Picker |
| `Super` + `E` / `Ctrl` + `Alt` + `F` | Open Thunar File Manager |
| `Alt` + `F2` / `Super` + `R` | Application Finder / Run Command |
| `Alt` + `F1` | Open XFCE Applications Menu |
| `Print` | Interactive Screenshot Tool |
| `Shift` + `Super` + `S` | Select Screen Area & Copy Screenshot to Clipboard |
| `Shift` + `Super` + `F` | Fullscreen Screenshot to Clipboard |
| `Alt` + `Print` | Active Window Screenshot |
| `Shift` + `Ctrl` + `Escape` | Open Task Manager |
| `Ctrl` + `Alt` + `Delete` | Logout / Power Options |
| `Ctrl` + `Alt` + `L` | Lock Screen |
| `Ctrl` + `Alt` + `Escape` | Kill Window (`xkill` cursor mode) |
| `Super` + `P` / `Display` | Quick Monitor / Display Switcher |
| `Alt` + `Super` + `Up` / `Down` | Increase / Decrease Active Window Opacity |

🪟 Window & Workspace Controls
| Shortcut | Action |
| :--- | :--- |
| `Alt` + `F4` | Close Active Window |
| `Alt` + `F10` | Toggle Maximize Window |
| `Alt` + `F9` | Minimize Window |
| `Alt` + `Tab` | Switch Between Open Windows |
| `Super` + `Left` / `Right` | Snap Window Left / Right |
| `Ctrl` + `Alt` + `Left` / `Right` | Switch Workspaces |

### 💡 Note on Keybind Overlaps & Layout Adaptations
You may notice multiple keybinds assigned to similar functions (for example, both Super + Space and Alt + F2 open application finders/launchers).

  **Why the duplicates?:** Designed to accommodate switching between different keyboard
  form factors (such as full-sized vs. compact/60% keyboards). Certain standard function 
  keys or key combos aren't easily accessible on smaller layouts without pressing an extra
  Fn layer, so secondary shortcuts keep navigation smooth on any keyboard size.
  
  **Customization:** You can edit or delete duplicate keybinds, or remap them entirely by
  opening Applications → Settings → Keyboard → Application Shortcuts.

  ## 🧩 Modular / Standalone Tools (Works on Any Distro & Desktop)
  The following configurations are standalone and can be used on Ubuntu, Debian, Fedora, Mint, Arch, or any other Linux distribution regardless of desktop environment:

```btop``` — Terminal system monitor layout

```rofi``` — Application launcher theme & keybindings

```bashpicom``` — Transparency, rounded corners, and shadow effects

```tint2``` — Standalone taskbar / panel design

## Single-Tool Copy Instructions
After cloning the repo, copy only the directory for the app you want:
 Copy Rofi theme only
 
```cp -r ~/dotfiles/rofi ~/.config/```

 Copy Tint2 panel config only
 
```cp -r ~/dotfiles/tint2 ~/.config/```

 Copy Btop config only
 
```mkdir -p ~/.config/btop && cp ~/dotfiles/btop/btop.conf ~/.config/btop/```

 Copy Picom compositor config only
 
```cp -r ~/dotfiles/picom ~/.config/```

## 🎨 Where to Find & Install Themes & Icons

Since desktop customization works independently of your Linux distribution, you can browse and download custom GTK themes, icon packs, cursors, and wallpapers directly from these site directories:

- **XFCE & Window Themes:** [xfce-look.org](https://www.xfce-look.org/)
- **GTK Themes, Icons & Cursors:** [pling.com](https://www.pling.com/) / [gnome-look.org](https://www.gnome-look.org/)
- **Cross-Distro Package Search:** [pkgs.org](https://pkgs.org)

### Manual Installation (Works on Any Distro)
1. **GTK / Desktop Themes:** Extract downloaded theme folders into `~/.themes/` (or `~/.local/share/themes/`).
2. **Icon & Cursor Packs:** Extract downloaded icon folders into `~/.icons/` (or `~/.local/share/icons/`).
3. **Apply Changes:** Open **Settings $\rightarrow$ Appearance** (or run `lxappearance` in terminal) to pick your newly installed themes and icon packs!
