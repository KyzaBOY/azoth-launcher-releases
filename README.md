# Azoth Launcher: downloads

This repository only hosts the **installers** of the Azoth Launcher, the desktop app of
[Project Azoth](https://projectazoth.com). There is no source code here.

## Download

Get the latest version from the [Releases page](https://github.com/KyzaBOY/azoth-launcher-releases/releases/latest)
and run `AzothLauncherSetup-<version>.exe`. It installs for your Windows user only (no admin prompt).

Once installed, the launcher updates itself: it checks `projectazoth.com` for the latest version and downloads
the installer from this repository. Every download is checked against the SHA-512 published by our server before it
is installed.

## Checking a download

Each release lists the SHA-256 of its files in `SHA256SUMS.txt`. On Windows:

```
certutil -hashfile AzothLauncherSetup-<version>.exe SHA256
```

The result must match the line in `SHA256SUMS.txt` of the same release.

## "My antivirus flagged it"

The installer is not code-signed yet, and the launcher patches the game in memory when it starts it (that is how it
points the client at our servers). Some antivirus products flag that pattern on unsigned programs. If yours does,
please tell us in the Discord with the name of the antivirus and the detection, so we can report the false positive.
