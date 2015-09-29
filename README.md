chromebrew
==========

Package manager for Chrome OS

ARM
---

This alpha version has limited **ARMv7** support (such as Rockchip RK3288 processor). It can install ruby with install.sh script.

However you will not be able to install packages. They have not been compiled yet on ARMv7. Interested in compiled packages? File an issue or contact [Heri](http://github.com/heri)

Overview
--------

Chromebooks with Chrome OS run a linux kernel - the only missing piece to use them as full-featured linux distro was gcc and make with their dependencies. Well, the piece isn't missing anymore. Say hello to chromebrew!

Installation
------------

Download and run the installation script for your ARM chromebook:

    wget https://raw.github.com/heri/chromebrew-arm/master/install.sh | bash

Usage
-----

    crew <command> <package> <keep[temporary files]>

Where available commands are:

  * search [looks for a package]
  * download [downloads a package to `CREW_BREW_DIR` (`/usr/local/tmp/crew` by default), but doesn't install it]
  * install [installs a package along with its dependencies. You'll be prompted for confirmation]
  * remove [removes a package. Must be ran as root]

Available packages are listed in the [packages directory](https://github.com/heri/chromebrew-arm/tree/master/packages).

Chromebrew will wipe its `BREW_DIR` (`/usr/local/tmp/crew` by default) after installation unless you pass "keep" as the last parameter when running "crew install".

    crew install <package> keep

License
-------

Copyright 2013 Michal Siwek


This project including all of its source files is released under the terms of [GNU General Public License (version 3 or later)](http://www.gnu.org/licenses/gpl.txt)
