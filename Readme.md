ghc-hack-day
------------

These are notes for running a GHC Hack Day, a day where experienced Haskell
developers are introduced to configuring, building, hacking on, testing and
debugging the [Glasgow Haskell Compiler] (GHC) as well on how to get help and
how to communicate with the GHC developer community.


# Location and Date

To be announced.


# Pre-requesites

You should be a reasonably experienced Haskell developer, know how to use
cabal-install and/or stack and know how to use git (knowing how to use
branches, rebasing commits and submodules will help).

You will also need a development machine (a laptop is the only real sane
alternative). I know how to set up a GHC build enviroment on both Linux and
on Mac OS X. Hopefully most people will be running on Linux on Mac OS X.
Building GHC on Windows is possible but more difficult. People on Windows may
want to set up a Virtual Machine running Ubuntu.

You will also need  a bunch of standard Open Source development tools including
but not limited to:

 - GNU gcc or Clang
 - GNU make
 - GNU autoconf
 - Perl
 - GHC (version 7.10.* or later)
 - python-sphinx
 - libgmp (including the header files, on Debian/Ubuntu this is libgmp-dev)
 - libncurses (on Debian/Ubuntu this is libncurses5-dev)

If you are interested in building GHC as a Linux or Mac to Android/Arm or
iOS/arm cross compiler you will also need llvm (versions 3.7 and 3.8) and a
working GNU GCC or Clang cross compile toolchain.

# Before the Hack Day

Before the Hack Day, you should make sure you have all the dev tools listed
above installed and you should also use git to clone the GHC repo. The GHC
repo is huge and the best way to do the initial clone is as follows:

```
mkdir ~/GHC
cd ~/GHC
git clone https://github.com/ghc/ghc.git ghc-upstream
cd ghc-upstream
sed -i 's|https://github.com/ghc|git://git.haskell.org|' .git/config
git submodule update --init --recursive --rebase
```

You should probably also have a go at [Building GHC] on your own. If you run
into trouble we can sort that out on the Hack Day.




[Glasgow Haskell Compiler]: https://ghc.haskell.org/trac/ghc/

[Building GHC]: https://ghc.haskell.org/trac/ghc/wiki/Building
