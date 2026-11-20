# Caesar native: releases

Installable packages of the native desktop client for
[Caesar](https://github.com/h8d13/caesar) servers, for Arch Linux.
The source lives in a separate, private repository.

## Install and stay up to date (recommended)

Add the repository to pacman once:

```
sudo tee -a /etc/pacman.conf <<'CONF'

[caesar-native]
SigLevel = Optional TrustAll
Server = https://github.com/nicoproto/caesar-native-releases/releases/download/repo
CONF
sudo pacman -Sy caesar-native
```

From then on Caesar updates with the rest of your system: `sudo pacman -Syu`.
The app also tells you when a new version is out.

## Install once, by hand

Download `caesar-native-<version>-1-x86_64.pkg.tar.zst` from the
[latest release](https://github.com/nicoproto/caesar-native-releases/releases/latest)
and run `sudo pacman -U caesar-native-<version>-1-x86_64.pkg.tar.zst`.

## Then

Open **Caesar** from your app launcher, enter your server's address and sign in.
Optional extras: `mpv` (watch party), `yt-dlp` (YouTube links), `1password-cli`,
`pipewire-pulse` (share screen audio).

Packages aren't signed yet (`SigLevel = Optional TrustAll`): they're trusted
because they come from this repository over HTTPS.
