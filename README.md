# GNOME Setup (Ubuntu 24.04)

These instructions install the standard GNOME desktop session, config utilities, and the current GNOME Shell extensions I regularly use.

> **Note:** Ubuntu 24.04 ships with **GNOME 46** by default.

## 1. Install GNOME Packages

```bash
sudo apt update
sudo apt install -y \
    gnome-session \
    gnome-tweaks \
    gnome-shell-extensions \
    gnome-shell-extension-manager
```

| Package | Description |
|---|---|
| `gnome-session` | Standard GNOME desktop session (instead of Ubuntu's customized session). |
| `gnome-tweaks` | Additional GNOME appearance and behavior settings. |
| `gnome-shell-extensions` | Collection of official GNOME Shell extensions. |
| `gnome-shell-extension-manager` | GUI for installing and managing GNOME extensions. |

To use standard GNOME, log out, select your username, click the gear icon, and select **GNOME** before logging in.

## 2. Install GNOME Extensions



| Extension | UUID | Purpose |
|---|---|---|
| [System Monitor Next](https://extensions.gnome.org/extension/3010/system-monitor-next/) | `system-monitor-next@paradoxxx.zero.gmail.com` | Display system statistics in the top panel. |
| [Named Workspaces](https://extensions.gnome.org/extension/9318/named-workspaces/) | `named-workspaces@a31.at` | Display descriptive workspace names in the top panel. |

**Install using Extension Manager:**

Launch **Extension Manager** from the application launcher, or run:

```bash
extension-manager
```

Select **Browse**, search for each extension, and install a version compatible with your GNOME Shell version.

> **Note:** The executable is `extension-manager`, not `gnome-shell-extension-manager` (the Ubuntu package name).

## Terminal

```bash
# Check GNOME Shell version
gnome-shell --version

# List all installed extensions
gnome-extensions list

# List enabled extensions
gnome-extensions list --enabled

# List disabled extensions
gnome-extensions list --disabled

# Enable extensions
gnome-extensions enable system-monitor-next@paradoxxx.zero.gmail.com
gnome-extensions enable named-workspaces@a31.at

# Disable extensions
gnome-extensions disable system-monitor-next@paradoxxx.zero.gmail.com
gnome-extensions disable named-workspaces@a31.at
```

If an extension does not appear immediately, log out and log back in.
