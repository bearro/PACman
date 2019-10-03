# pacman

PAC wallet/daemon management utilities - version 0.1.28

* This script installs, updates, and manages single-user pac daemons and wallets
* It is currently only compatible with 32/64 bit linux.
* Multi-user (system directory) installs are not supported

# Install/Usage

To install pacman do:

    sudo apt-get install python git unzip pv && cd ~ && git clone https://github.com/bearro/pacman

    cd ~ && git clone https://github.com/bearro/pacman

    git clone git@github.com:Bearro/pacman.git

    sudo chown -R ~/pacman

    find /pacman -type d -exec chmod 755 {} \;

    cd pacman && git config core.filemode false

==Info on source code binaries to compile:==
Info:https://github.com/barrystyle/PAC/blob/develop/doc/build-unix.md
Info2:https://github.com/barrystyle/PAC/blob/develop/doc/build-generic.md

wget https://github.com/PACGlobalOfficial/PAC/archive/24c14bbb7.tar.gz
mkdir /root/pacraw
tar -xzvf 24c14bbb7.tar.gz -C /root/pacraw

==One liner re-test Bearro:==

sudo rm -rf .pacglobal && sudo rm -rf pacman && cd ~ && git clone https://github.com/bearro/pacman && chmod -R 755 pacman && pacman/bin/pacman.sh install



To delete pacman do:

    sudo rm -rf pacman

To update your existing version 12 32/64bit linux pac wallet to the latest
pacglobald, do:

    pacman/pacman update

To perform a new install of pac, do:

    pacman/pacman install

To overwrite an existing pac install, do:

    pacman/pacman reinstall

To update pacman to the latest version, do:

    pacman/pacman sync

To restart (or start) pacglobald, do:

    pacman/pacman restart

To get the current status of pacglobald, do:

    pacman/pacman status


# Commands

## sync

"pacman sync" updates pacman to the latest version from github

## install

"pacman install" downloads and initializes a fresh pac install into ~/.pacglobal
unless already present

## reinstall

"pacman reinstall" downloads and overwrites existing pac executables, even if
already present

## update

where it all began, "pacman update" searches for your pacglobald/pacglobal-cli
executibles in the current directory, ~/.pacglobal, and $PATH.  It will prompt
to install in the first directory found containing both pacglobald and pacglobal-cli.
Multiple wallet directories are not supported. The script assumes the host runs
a single instance of pacglobald.

## restart

"pacman restart [now]" restarts (or starts) pacglobald. Searches for pacglobal-cli/pacglobald
the current directory, ~/.pacglobal, and $PATH. It will prompt to restart if not
given the optional 'now' argument.

<a href="#restart-1">screencap</a>

## status

"pacman status" interrogates the locally running pacglobald and displays its status

<a href="#status-1">screencap</a>

# Dependencies

* bash version 4
* nc (netcat)
* curl
* perl
* pv
* python
* unzip
* pacglobald, pacglobal-cli - version 12 or greater to update

# Screencaps

### install

<img src="https://raw.githubusercontent.com/bearro/pacman/master/screencaps/pacman_0.1-install.png">

### update

<img src="https://raw.githubusercontent.com/bearro/pacman/master/screencaps/pacman_0.1-update.png">

### reinstall

<img src="https://raw.githubusercontent.com/bearro/pacman/master/screencaps/pacman_0.1-reinstall.png">

### restart

<img src="https://raw.githubusercontent.com/bearro/pacman/master/screencaps/pacman_0.1-restart.png">

### status

<img src="https://raw.githubusercontent.com/bearro/pacman/master/screencaps/pacman_0.1-status.png">

# Contact

Email me at bearro@masternode.me or submit a pull request.
