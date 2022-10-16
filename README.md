# Mirraur

A server-side AUR helper of a dream, finally been made real.


# Description

The basic idea is to emulate a [Pacman](https://archlinux.org/pacman/) repository to manage AUR packages with on-demand and/or automated builds & updates.

The (planned) ecosystem consists of these parts:

  * Server-side (`mirraur`):
    - [ ]  Pacman mirror emulator
    - [ ]  Package build server
    - [ ]  Repository DB manager daemon
    - [ ]  Version & dependency checker
    - [ ]  AUR scraper
    - [ ]  Email subscription client (for reliable update tracking of important packages)
    - [ ]  Client RPC API
  * Client-side (`yr`):
    - [ ]  AUR package search
    - [ ]  Stateless OTP Auth on server
    - [ ]  Build status check
    - [ ]  Pacman's `.pac*` files management
    - [ ]  Managing package upgrades, either of:
      * Upstream tracking request to Mirraur, or
      * Local update checking (in which case the server would possibly be stateless)

Among planned features are:

  - [ ]  Client-defined custom build options (such as CPU architecture flags for optimizations)
  - [ ]  Interactive building status update via HTTP redirects in Pacman itself while downloading the package
  - [ ]  Parallel downloading/building support
  - [ ]  Various limits with task queue
  - [ ]  Automatic configurable package & source clean-ups
  - [ ]  Manual intervention mode for when an automatic build fails (probably through an ssh session into a temporary container/chroot using `yr` with a result of `PKGBUILD.patch` generation)


# FAQ

* **Why write everything in a huge mono-file?**<br>
Multiple files scare me. I like scrolling more than clicking or, even worse, --- browsing.<br>
Also, my source code browser likes this.

* **Why `asyncio`?**<br>
Trying to be sleek!

* **Why the client is named `yr`?**<br>
It's a tribute in loving memory to [Yaourt](https://github.com/archlinuxfr/yaourt), to which I used to have a bash alias of that name a long time before Mirraur came to life.

* **How to pronounce «Mirraur»?**<br>
Just like 'mirror', but with a bit longer '[ə]'. Or like 'mirr-our', I can't tell if these are any different :P


###### P.S. Trackballs are a great thing. Just saying.
