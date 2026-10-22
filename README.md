# archdi

Just a simple bash script wizard to install and configure a full personal computer with Arch Linux.

This is a maintained fork of [MatMoul/archdi](https://github.com/MatMoul/archdi), updated for current Arch Linux.

First, install Arch Linux with the official media and optionally with archfi.<br />
Look at archfi project to start your arch linux installation : https://github.com/sevenzip2/archfi

After reboot and your network ready, download the script:

    curl -fsSL https://raw.githubusercontent.com/sevenzip2/archdi/master/archdi -o archdi

And run the script:

    sh archdi

Or you can install it on your system with:

    sh archdi -i

And then you can use archdi cmd.<br />
With this, you can make your updates or install your packages later.

You can watch the original author's videos to show how to use it :<br />
https://www.youtube.com/playlist?list=PLytHgIKLV1caHlCrcTSkm5OF2WSVI1_Sq

## Repository layout

- `archdi` : the launcher, it downloads the `pkg/` folder of this repository and starts it
- `pkg/lib` : shared functions (package install, AUR helpers, services, sudoers...)
- `pkg/menu`, `pkg/install`, `pkg/config`, `pkg/updates`, `pkg/shutdown` : the menus

The menus used to live in the separate archdi-pkg repository, they were merged here with their history.

## For developers

Test a branch of your fork :

    archdi -t {githubusername} {branchname}

Test a branch of sevenzip2/archdi :

    archdi -b {branchname}

Run a local copy of the menus :

    archdi -l /path/to/archdi/pkg
