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

## Syncing (-S)

1. `pacman -S <package name>`

        Installs the specified package from official repos.
    <details>
    <summary>Click to see example</summary>
    $ sudo pacman -S xclip </br>
    [sudo] password for username: 
    resolving dependencies...
    looking for conflicting packages...

    Packages (1) xclip-0.13-3

    Total Installed Size:  0.03 MiB
    Net Upgrade Size:      0.00 MiB

    :: Proceed with installation? [Y/n]
    </details>

2. `pacman -Ss <regexp>`

        Searches for packages using a regular expression in the local repo. 
    <details>
    <summary>Click to see example</summary>
    $ pacman -Ss clip </br>
    extra/eclipse-ecj 4.6.3-2 </br>
    &nbsp;&nbsp;&nbsp;&nbsp;Eclipse java bytecode compiler </br>
    extra/gpaste 3.38.5-1 </br>
    &nbsp;&nbsp;&nbsp;&nbsp;Clipboard management system </br>
    extra/xclip 0.13-3 [installed] </br>
    &nbsp;&nbsp;&nbsp;&nbsp;Command line interface to the X11 clipboard </br>
    extra/xfce4-clipman-plugin 1.6.1-1 (xfce4-goodies) </br>
    &nbsp;&nbsp;&nbsp;&nbsp;A clipboard plugin for the Xfce4 panel </br>
    extra/xorg-xclipboard 1.1.3-3 </br>
    &nbsp;&nbsp;&nbsp;&nbsp;X clipboard manager </br>
    </details>


3. `pacman -Syu`

        Refresh sync databases and upgrade packages.
    <details>
    <summary>Click to see example</summary>
    $ sudo pacman -Syu</br>
    [sudo] password for username: </br>
    :: Synchronizing package databases...</br>
    core is up to date</br>
    extra is up to date</br>
    community is up to date</br>
    multilib is up to date</br>
    :: Starting full system upgrade...</br>
    there is nothing to do</br>

4. `pacman -Si <package name>`

        Outputs verbose information about the found package in the official repos.
    <details>
    <summary>Click to see example</summary>
    $ pacman -Si xclip </br>
    Repository : extra </br>
    Name : xclip </br>
    Version : 0.13-3 </br>
    Description : Command line interface to the X11 clipboard </br>
    Architecture : x86_64 </br>
    URL : https://github.com/astrand/xclip </br>
    Licenses : GPL </br>
    Groups : None </br>
    Provides : None </br>
    Depends On : libxmu </br>
    Optional Deps : None </br>
    Conflicts With : None </br>
    Replaces : None </br>
    Download Size : 14.98 KiB </br>
    Installed Size : 34.39 KiB </br>
    Packager : Felix Yan <felixonmars@archlinux.org> </br>
    Build Date : Sat 16 May 2020 03:56:14 PM UTC </br>
    Validated By : MD5 Sum SHA-256 Sum Signature </br>
    </details>

5. `pacman -Sg <group name>`

        Lists all the packages that are in a group.
    <details>
    <summary>Click to see example</summary>
    $ pacman -Sg base-devel</br>
    base-devel autoconf </br>
    base-devel automake </br>
    base-devel binutils </br>
    base-devel bison </br>
    base-devel fakeroot </br>
    base-devel file </br>
    base-devel findutils </br>
    base-devel flex </br>
    base-devel gawk </br>
    base-devel gcc </br>
    base-devel gettext </br>
    base-devel grep </br>
    base-devel groff </br>
    base-devel gzip </br>
    base-devel libtool </br>
    base-devel m4 </br>
    base-devel make </br>
    base-devel pacman </br>
    base-devel patch </br>
    base-devel pkgconf </br>
    base-devel sed </br>
    base-devel sudo </br>
    base-devel texinfo </br>
    base-devel which </br>
    </details>

6. `pacman -Sw <package name>`

        Downloads a package from the official repos.
    <details>
    <summary>Click to see example</summary>
    [sudo] password for username: 
    $ sudo pacman -Sw xclip </br>

    resolving dependencies...

    Packages (1) xclip-0.13-3

    Total Download Size:  0.00 MiB

    :: Proceed with download? [Y/n] 
    </details>

7. `pacman -Sc`

        Removes packages from local cache
    <details>
    <summary>Click to see example</summary>
    $ sudo pacman -Sc</br>
    [sudo] password for username: </br>
    Packages to keep:</br>
    All locally installed packages</br>

    Cache directory: /var/cache/pacman/pkg/</br>
    :: Do you want to remove all other packages from cache? [Y/n]</br>
    </details>

