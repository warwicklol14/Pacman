# Pacman commands

## Querying (-Q)

1. `pacman -Q <package name>`

        Outputs name of the found package in the local repo and it's current installed version. 
    <details>
    <summary>Click to see example</summary>
    $ pacman -Q xclip </br>
    xclip 0.13-3
    </details>

2. `pacman -Qi <package name>`

        Outputs verbose information about the found package in the local repo.
    <details>
    <summary>Click to see example</summary>
    $ pacman -Qi xclip </br>
    Name            : xclip </br>
    Version         : 0.13-3 </br>
    Description     : Command line interface to the X11 clipboard </br>
    Architecture    : x86_64 </br>
    URL             : https://github.com/astrand/xclip </br>
    Licenses        : GPL </br>
    Groups          : None </br>
    Provides        : None </br>
    Depends On      : libxmu </br>
    Optional Deps   : None </br>
    Required By     : None </br>
    Optional For    : None </br>
    Conflicts With  : None </br>
    Replaces        : None </br>
    Installed Size  : 34.39 KiB </br>
    Packager        : Felix Yan <felixonmars@archlinux.org> </br>
    Build Date      : Sat 16 May 2020 03:56:14 PM UTC </br>
    Install Date    : Sun 21 Feb 2021 11:09:59 AM UTC </br>
    Install Reason  : Explicitly installed </br>
    Install Script  : No </br>
    Validated By    : Signature </br>
    </details>

3. `pacman -Ql <package name>`

        Lists the files installed by the found package in the local repo.
    <details>
    <summary>Click to see example</summary>
    $ pacman -Ql xclip </br>
    xclip /usr/ </br>
    xclip /usr/bin/ </br>
    xclip /usr/bin/xclip </br>
    xclip /usr/bin/xclip-copyfile </br>
    xclip /usr/bin/xclip-cutfile </br>
    xclip /usr/bin/xclip-pastefile </br>
    xclip /usr/share/ </br>
    xclip /usr/share/man/ </br>
    xclip /usr/share/man/man1/ </br>
    xclip /usr/share/man/man1/xclip-copyfile.1.gz </br>
    xclip /usr/share/man/man1/xclip.1.gz </br>
    </details>

4. `pacman -Qo <file>`

        Outputs the package which owns the specified file.
    <details>
    <summary>Click to see example</summary>
    $ pacman -Qo /usr/include/SDL2/SDL.h </br>
    /usr/include/SDL2/SDL.h is owned by sdl2 2.0.14-1
    </details>

5. `pacman -Qe`

        Outputs the explicitly installed packages.
    <details>
    <summary>Click to see example</summary>
    $ pacman -Qe </br>
    acpi 1.7-3 </br>
    acpid 2.0.32-2 </br>
    alsa-firmware 1.2.4-2 </br>
    alsa-utils 1.2.4-2 </br>
    android-tools 30.0.5-1 </br>
    android-udev 20201003-1 </br>
    apparmor 3.0.1-1 </br>
    appimagelauncher 2.2.0-4 </br>
    ark 20.12.2-1 </br>
    autoconf 2.71-1 </br>
    ...
    </details>


6. `pacman -Qm`

        Outputs the foreign packages such as those installed from AUR (Arch User Repo)
    <details>
    <summary>Click to see example</summary>
    $ pacman -Qm</br>
    plex-media-player 2.58.0-4 </br>
    ttf-ms-fonts 2.0-12 </br>
    </details>

7. `pacman -Qdt`

        Outputs the orphan packages (packages that were installed as dependencies but are no longer needed)
    <details>
    <summary>Click to see example</summary>
    $ pacman -Qdt</br>
    go 2:1.48.0-2 </br>
    </details>

8. `pacman -Qs <regexp>`

        Searches for packages using a regular expression in the local repo.
    <details>
    <summary>Click to see example</summary>
    $ pacman -Qs clip</br>
    local/xclip 0.13-3 </br>
    &nbsp;&nbsp;&nbsp;&nbsp;Command line interface to the X11 clipboard </br>

    </details>

