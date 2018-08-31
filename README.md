# RADDI: *Windows builds*

This repository follows structure: /architecture/build/executable

## Architectures

* **x86-32** - for 32-bit Windows, uses slighly less RAM; will run on any Windows device (x64/arm64)
* **x86-64** - for 64-bit Windows, **recommended**
* **arm-64** - *planned for AArch64 devices running Windows*

## Builds

* **release**
 - small executables, need libraries from https://github.com/raddinet/raddi-redist-windows
 - lower memory usage as the DLLs and MSVCRT are shared in memory
 - allows replacing provided DLLs with custom built or official ones if you don't trust those provided above
 - Windows Vista or newer is required

* **portable**
 - no need to download and install anything else, all libraries compiled in
 - larger executables and slighly higher memory usage
 - Windows XP (5.1 for x86-32, 5.2 for x86-64)

## Executables

* **raddi32.exe**/**raddi64.exe** - node software, runs on background and participates in the network
* **raddi.com** - command-line utility
* **raddi.exe** - *not yet available, GUI client app*

## Installer

*TBD*