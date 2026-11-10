<p align="center"><img src="docs/images/masterkey.svg" width="96" alt="MasterKey"></p>

<h1 align="center">MasterKey — releases</h1>

<p align="center">
  <a href="https://github.com/lugio/masterkey-versions/releases/latest"><img alt="Latest release" src="https://img.shields.io/github/v/release/lugio/masterkey-versions?label=version"></a>
  <img alt="Platform" src="https://img.shields.io/badge/platform-Windows-0078d4">
  <img alt="Signed updates" src="https://img.shields.io/badge/updates-signed%20(minisign)-2ea043">
</p>

<p align="center"><a href="README.fr.md">Français</a></p>

**MasterKey** is a desktop connection manager written in Rust (Tauri 2, Vue 3): SSH and RDP in tabs, a bookmark tree, a local
encrypted vault and a read-only link to Bitwarden / Vaultwarden. Its source code is private until version 1.

This repository holds **no code**. It publishes the signed Windows installers, their signatures and the `latest.json` file that
MasterKey reads to offer updates.

## Updates from inside the app

When a newer version is published here, its number shows up next to the logo, in the title bar:

![Update notice in the title bar](docs/images/avis.png)

One click shows what changed and offers **Install and restart**. Nothing is installed without that click, and open sessions are
listed before the restart:

![Update dialog](docs/images/dialogue.png)

*(Screenshots taken on the built-in sample bookmarks.)*

## Integrity

- Every installer is signed with minisign. The public key is built into MasterKey, which **refuses any file whose signature does
  not match**, wherever it comes from.
- The private key never leaves the maintainer's workstation; continuous integration does not sign anything.
- The installers themselves are not yet Authenticode-signed: Windows SmartScreen will warn on the first manual install.

## Install

1. Download `MasterKey_x.y.z_x64-setup.exe` from the [latest release](https://github.com/lugio/masterkey-versions/releases/latest).
2. Run it (per-user install, no administrator rights needed).
3. Later versions arrive through the notice in the title bar.

Until version 1, every release is a **test build**, for evaluation (published as a regular release so that the update feed can find it).

## License

See [LICENSE](LICENSE): private until version 1, then an open-source license is planned.
