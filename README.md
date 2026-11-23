# OrkaLinux packages

The apt repository for [OrkaLinux](https://github.com/cyz-yt/OrkaLinux). It brings fixes and new versions of the OrkaLinux apps, login screens and wallpapers to systems that are already installed - no need to install the system again.

OrkaLinux B3 and newer already use it. Updates come in with the rest of the system: **Update** in OrkaLinux Centrum, Discover, or `sudo apt update && sudo apt full-upgrade`.

## What's inside

| Package | What it is |
|---|---|
| `orkalinux-base` | OrkaLinux Hello, OrkaLinux Centrum, Wygląd systemu (Look), Kopia zapasowa (Backup), the Glass and Side panel login screens, the Plasma look and the icons |
| `orkalinux-wallpapers` | The OrkaLinux wallpapers |
| `orkalinux-archive-keyring` | The key this repository is signed with |

Everything is built from the files in the [OrkaLinux repository](https://github.com/cyz-yt/OrkaLinux).

## Adding it by hand

OrkaLinux B3 has it set up already. If you removed it, this adds it back - first the key, then the source:

```
sudo curl -fsSL -o /usr/share/keyrings/orkalinux-archive-keyring.gpg https://cyz-yt.github.io/orkalinux-repo/orkalinux-archive-keyring.gpg
```

```
printf 'Types: deb\nURIs: https://cyz-yt.github.io/orkalinux-repo\nSuites: stable\nComponents: main\nSigned-By: /usr/share/keyrings/orkalinux-archive-keyring.gpg\n' | sudo tee /etc/apt/sources.list.d/orkalinux.sources
```

```
sudo apt update && sudo apt install orkalinux-base orkalinux-wallpapers orkalinux-archive-keyring
```

The key fingerprint is in [`orkalinux-archive-keyring.asc`](orkalinux-archive-keyring.asc) - check it with `gpg --show-keys orkalinux-archive-keyring.asc`.

## Something broke after an update?

Tell me on [Discord](https://discord.gg/JkC9P6ebN2) or open an issue in the [OrkaLinux repository](https://github.com/cyz-yt/OrkaLinux/issues).

## More from the same author

- [OrkaLinux](https://github.com/cyz-yt/OrkaLinux): a Linux distribution built on Debian 13 with KDE Plasma 6.
- [OrkaPlayer](https://github.com/cyz-yt/OrkaPlayer): a media player with lyrics that sing along, karaoke, radio, TV and podcasts.
- [OrkaNote](https://github.com/cyz-yt/OrkaNote): a Notepad for Windows with tabs that come back, colours for code, Run (F9) for scripts and a dark theme.
- [OrkaPaint](https://github.com/cyz-yt/OrkaPaint): a drawing program for Windows - a bit more than plain Paint, with layers, selections and effects.
- [cyz's ISO Creator](https://github.com/cyz-yt/cyzs-ISO-Creator): makes an ISO file from a folder - for getting documents into a virtual machine without VMware Tools.
