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

## Requirements
* Scoop & WinGet
* Windows 10 / 11 (x64)
* Git
* JetBrains Mono Nerd Font

## Network Settings

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


