<div align="center">

<h1><img src="https://github.com/user-attachments/assets/53a351f9-bb27-4aa9-8dc3-8d4a4858cb43" width="56" align="middle" alt="">&nbsp;MooTTY</h1>

**A portable, offline, hardware-key-first SSH + SFTP client.**
One small binary for Windows, macOS and Linux. No account, no cloud, no telemetry.

[![Latest release](https://img.shields.io/github/v/release/chasgames/MooTTY?label=release&color=7ee0a3)](https://github.com/chasgames/MooTTY/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/chasgames/MooTTY/total?label=downloads&color=7ee0a3)](https://github.com/chasgames/MooTTY/releases)
[![Stars](https://img.shields.io/github/stars/chasgames/MooTTY?label=stars&color=e3c56b)](https://github.com/chasgames/MooTTY/stargazers)

[![Windows | macOS | Linux, 13 MB](https://img.shields.io/badge/Windows%20%7C%20macOS%20%7C%20Linux-13%20MB-2472c8)](https://github.com/chasgames/MooTTY/releases/latest)

![Made in Jersey](https://img.shields.io/badge/Made%20in-Jersey%20%F0%9F%87%AF%F0%9F%87%AA-e8112d)
![Approved by Jersey Cows](https://img.shields.io/badge/Approved%20by-Jersey%20Cows%20%F0%9F%90%84-a1785a)

</div>

## Screenshots

<div align="center">

<img width="1180" height="777" alt="MooTTY screen1" src="https://github.com/user-attachments/assets/647aae6a-5c4d-44be-ae47-522cadb410d0" />

<img width="1180" height="777" alt="MooTTY plot" src="https://github.com/user-attachments/assets/df40a218-09d7-4d01-ac44-75526f9a45f6" />


</div>

## Download

From the [latest release](https://github.com/chasgames/MooTTY/releases/latest):

| OS | File | Notes |
| --- | --- | --- |
| Windows | `MooTTY-windows-amd64.exe` / `-arm64.exe` | Just run it. |
| macOS | `MooTTY-darwin-universal.zip` | Unzip, then right-click > **Open** once (not notarized). |
| Linux | `MooTTY-linux-amd64` / `-arm64` | `chmod +x` and run. Needs `gtk3` + `libwebkit2gtk-4.1`. |



## Quick start

1. Type `user@host` in Quick Connect, or press **+** to save a host.
2. Connect. With a resident YubiKey credential there is no key file: plug in,
   PIN once, tap.
3. That one touch covers the terminal **and** SFTP.
4. Drag files onto the window to upload them to the current remote folder.

> `-sk` keys need a modern ssh-agent (OpenSSH 9.5+). Windows' built-in 8.6
> agent cannot sign them. Click the **openssh** chip and MooTTY sets up the
> portable agent it bundles.

## Features

| Feature | MooTTY | Popular alternative |
| --- | :---: | :---: |
| **Cross-platform** One codebase, native app on Windows, macOS and Linux | ✅ | ❌ |
| **FIDO2 / YubiKey `-sk` keys** Including resident (discoverable) credentials: no key file, plug in, PIN once, tap | ✅ | ❌ |
| **Real agent signing** No re-implemented crypto, touch happens at the actual signing moment, and one touch covers the terminal *and* SFTP | ✅ | ❌ |
| **Agent orchestration** Bundled portable OpenSSH, one-click Windows agent setup, diagnostics that name the exact `-sk` agent problem | ✅ | ❌ |
| **No strings** No account, no cloud broker, no telemetry | ✅ | ❌ |
| **Portable** Config, `known_hosts` and logs live next to the executable | ✅ | ✅ |
| **Lightweight** Single self-contained binary (~13 MB) on the native OS webview, not Electron, fully offline at startup | ✅ | ❌ |
| **Your own sync** Settings and host list sync through a secret gist on your GitHub account | ✅ | ❌ |
| **Keychain passwords** Stored by the OS, never in the config file, never synced | ✅ | ❌ |
| **Live plot** Click any number in terminal output and graph it over time | ✅ | ❌ |
| **Port forwarding** Local, remote and dynamic SOCKS tunnels | ✅ | ✅ |
| **Integrated SFTP** Same connection, drag-and-drop upload, recursive folder download, download-as-zip, open remote files locally | ✅ | ✅ |
| **Follow mode** The SFTP panel tracks the terminal's working directory | ✅ | ❌ |
| **Multi-session** Tabs, split layouts (columns / rows / grid) and broadcast typing to every terminal | ✅ | ✅ |
| **Jump hosts** Bastions configurable per host and per folder | ✅ | ✅ |
| **Imports** Reads `~/.ssh/config` and `/etc/hosts` | ✅ | ✅ |
| **Remote host sources** Pulls a connected server's own `/etc/hosts` and `~/.ssh/config` as live host lists | ✅ | ❌ |
| **Saved commands** Snippet panel with folders, search and sync | ✅ | ✅ |
| **Key tooling** In-app key generation, copy-key-to-host, and an ssh-agent key manager with fingerprints | ✅ | ❌ |
| **Session logging** Size cap and rotation that always keeps the newest output | ✅ | ✅ |
| **Host key safety** TOFU with a SHA256 fingerprint dialog, mismatch is a hard fail | ✅ | ✅ |
| **Modern terminal** xterm.js with true colour, scrollback minimap lens, font picker, native clipboard | ✅ | ✅ |
| **Safe updates** Built-in self-update and a forward-compatible config a newer version cannot break | ✅ | ❌ |

"Popular alternative" is a typical full-featured commercial GUI SSH client.

## TODO

| Feature | MooTTY | Popular alternative |
| --- | :---: | :---: |
| **X11 server** Built-in display server for remote GUI apps | ❌ | ✅ |
| **Other protocols** RDP, VNC, Telnet, serial, FTP | ❌ | ✅ |
| **Local toolchain** Bundled Unix shell environment | ❌ | ✅ |
| **Extensibility** Plugin ecosystem and macro scripting | ❌ | ✅ |
