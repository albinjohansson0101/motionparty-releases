# Motion Party for Windows

Party games on your TV. Phones are the controllers: scan a QR code, no app needed. Gamepads and keyboards work too.

This repository only hosts the Motion Party installers and update files. It contains no source code.

## Install

1. Open the [latest release](https://github.com/albinjohansson0101/motionparty-releases/releases/latest).
2. Download `MotionParty-Setup-<version>.exe` and run it.
3. Windows asks for permission to install for all users and to let phones on your private network connect.

**Windows SmartScreen** may show "Windows protected your PC", because the installer is not code-signed yet. Choose **More info → Run anyway** only if you downloaded it from the link above. To check the file first, compare its SHA-256 with `SHA256SUMS.txt` in the same release:

```powershell
Get-FileHash .\MotionParty-Setup-<version>.exe -Algorithm SHA256
```

Requirements: Windows 10 or 11 (64-bit). Phones and the PC must be on the same Wi-Fi network.

## Updates

Motion Party updates itself. It checks GitHub when it starts and every few hours, downloads new versions in the background, and asks before installing. Updates are verified with a digital signature and never interrupt a running game. Your settings, profile and installed games are kept.

**Settings → Updates** shows your version and lets you check now.

## Uninstall

Windows Settings → Apps → Motion Party → Uninstall. Your settings and games stay in `%APPDATA%\Motion Party`; delete that folder to remove them too.

## Files in a release

| File                                       | What it is                                        |
| ------------------------------------------ | ------------------------------------------------- |
| `MotionParty-Setup-<version>.exe`          | The installer                                     |
| `MotionParty-Setup-<version>.exe.blockmap` | Used by the updater to download only what changed |
| `latest.yml`, `latest.yml.sig`             | The signed update feed read by installed copies   |
| `SHA256SUMS.txt`                           | Checksums for manual verification                 |

Releases named **beta** are test builds for the beta channel. Normal installs never update to them.

© 2026 Bork Builds. All rights reserved.
