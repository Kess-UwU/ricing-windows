<p align="center">
  <img src="icon.png" alt="Windows 10 rice">
</p>

<div align="center">

<table border="1" width="100%" cellpadding="10" cellspacing="0">
  <thead>
    <tr bgcolor="#f0f0f0">
      <th colspan="2">All apps & settings</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>🔳Tackyborders</td>
      <td>💻Win. Terminal</td>
    </tr>
    <tr>
      <td>🖼️Qview</td>
      <td>🖼️Wallpaper pack</td>
    </tr>
    <tr>
      <td>📊YASB</td>
      <td>💧Rainmeter</td>
    </tr>
    <tr>
      <td>🎵CAVA</td>
      <td>💻TaskBarX</td>
    </tr>
    <tr>
      <td>🌐Brave</td>
      <td>⚙️Fastfetch</td>
    </tr>
    <tr>
      <td>🎮Steam</td>
      <td>🌐Network settings</td>
    </tr>
  </tbody>
</table>
</div>

# Requirements
* Scoop & WinGet
* Windows 10 / 11 (x64)
* Git
* JetBrains Mono Nerd Font

# Network Settings

```powershell
ipconfig /flushdns

netsh interface ipv4 set dns name="Ethernet 2" source=static address=1.1.1.1
netsh interface ipv4 add dns name="Ethernet 2" address=1.0.0.1 index=2

powershell -Command "Enable-NetAdapterBinding -Name 'Ethernet 2' -ComponentID 'ms_tcpip6'" 2>\$null
netsh interface ipv6 set dns name="Ethernet 2" source=static address=2606:4700:4700::1111 2>\$null
netsh interface ipv6 add dns name="Ethernet 2" address=2606:4700:4700::1001 index=2 2>\$null
```

> [!TIP]
> If your network adapter has a different name, replace `name="Ethernet 2"` with your actual adapter name (e.g., `name="Ethernet"` or `name="Wi-Fi"`).

# How to install

## 🛠️ Installation apps

First, open **PowerShell as Administrator** and install Scoop if you don't have it yet:

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope Process -Force
irm https://scoop.sh | iex
scoop bucket add extras
scoop bucket add nerd-fonts
```

Now, run the specific command for each application you want to install:

### 1. Core Tools & Fonts
* **Git**
  ```powershell
  scoop install git
  ```
* **Fastfetch**
  ```powershell
  scoop install fastfetch
  ```
* **JetBrains Mono Nerd Font**
  ```powershell
  scoop install jetbrainsmono-nf
  ```

### 2. Interface, Bars & Tiling
* **YASB** (Status bar)
  ```powershell
  scoop install yasb
  ```
* **GlazeWM / Rainmeter** (Window manager & widgets)
  ```powershell
  scoop install glazewm rainmeter
  ```
* **TaskbarX** (Taskbar centering tool)
  ```powershell
  scoop install taskbarx
  ```

### 3. Media & Viewers
* **CAVA** (Audio visualizer via WinGet)
  ```powershell
  winget install karlstav.cava   
  ```
* **Qview** (Minimal image viewer)
  ```powershell
  scoop install qview
  ```
* **Brave browser**
  ```powershell
  scoop install brave
  ```

### 4. Manual Installation
* **Tackyborders** — [Download from Official GitHub Releases](https://github.com/lukeyou05/tacky-borders/releases)
* **Millenium for steam** — [Download from Official GitHub Releases](https://github.com/SteamClientHomebrew/Millennium/releases)

## 🎮 Steam Theme Setup

1. Open Steam and open the **Millennium** dashboard.
2. Go to the themes section.
3. Paste the following theme ID into the field:
   ```text
   zQndv1rI0FXLh3QTRgOL
   ```
4. Save the settings and reload Steam to apply the skin.

## 🌐 Brave Browser Setup

* Chrome Theme: [Catppuccin mocha theme](https://chromewebstore.google.com/detail/catppuccin-chrome-theme-m/bkkmolkhemgaeaeggcmfbghljjjoofoh)
* Stylus file location: `dots/stylus` (Open Stylus -> **Import** -> Select this file)

