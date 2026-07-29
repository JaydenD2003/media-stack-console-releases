# Media Stack Console — downloads

This repository holds the installer and the update manifest for Media Stack
Console. It contains no source code; the application itself is developed
privately.

## Install

Download the latest `MediaStackConsole-Setup-x.y.z.exe` from
[Releases](../../releases/latest) and run it.

The installer is not code-signed, so Windows SmartScreen will show a warning
before it runs. Choose **More info**, then **Run anyway**. The checksum of every
release is published on its release page and in `latest`, so a download can be
verified before it is trusted:

```powershell
Get-FileHash .\MediaStackConsole-Setup-x.y.z.exe -Algorithm SHA256
```

## What it is

A Windows console for a self-hosted media stack: Jellyfin, qBittorrent behind a
VPN, and the Prowlarr, Radarr, Sonarr and Bazarr chain. It runs the stack in
Docker on the same PC, or drives one on a separate Linux server over SSH.

Setup is guided. Docker is installed for you if it is missing, the stack is
generated and started, and the services are wired together — nothing is
installed without being listed and agreed to first.

## Requirements

- Windows 10 version 1809 or later, 64-bit
- A VPN account that permits P2P
- For a local stack: virtualisation enabled in firmware, and about 12 GB free

## Updates

`latest` is the manifest the application reads to notice a new version. It is
plain JSON and points at the release asset for that version.
