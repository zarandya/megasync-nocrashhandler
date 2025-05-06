# megasync-nocrashhandler
MEGAsync with the crash handler removed, allows building MEGAsync on aarch64 and other non-supported architectures.

I am not affiliated with Mega. 

## Install instructions

First, [install flatpak and set up flathub](https://flathub.org/setup) (required to download dependencies).
Then, download the prebuilt .flatpak from [GitHub releases](https://github.com/zarandya/megasync-nocrashhandler/releases), and install it with
```
flatpak install --user /path/to/nz.mega.MEGAsync-version_number.aarch64.flatpak
```

----

Or, if you want to manually build it, install `flatpak`, `flatpak-builder`, and use `flatpak` to install `org.kde.Sdk`. 

`flatpak-builder --user --install --force-clean build nz.mega.MEGAsync.yml`

The app will run insude the flatpak sandbox and won't have filesystem access. Use `flatpak override...` or flatseal to give it access to the directory where you want to store the synced files. 

