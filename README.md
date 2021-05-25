# RADDI: *Windows builds*

This repository follows structure: /architecture/build/executable

## Architectures

* **x86-32** - for 32-bit Windows, uses slighly less RAM; will run on any Windows PC (x64/arm64)
* **x86-64** - for 64-bit Windows, **recommended**
* **arm-64** - for AArch64 devices running 64-bit Windows 10 for ARM

## Builds

* **release**
  - small executables, need libraries from https://github.com/raddinet/raddi-redist-windows
  - lower disk/memory usage as the DLLs and MSVCRT are shared both on disk and in memory
  - allows for replacing/upgrading DLLs with custom built or official ones if you don't trust those provided above

* **portable**
  - no need to download and install anything else, all libraries compiled in
  - larger executables and slighly higher memory usage

## Executables

* **raddi32.exe**/**raddi64.exe** - node software, runs on background and participates in the network
* **raddi.com** - command-line utility
* **raddi.exe** - *not yet available, basic GUI client app*

## Minimal OS Version Requirements

Generally **Windows XP** (5.1 for x86-32, 5.2 for x86-64) or later is required with following exceptions:

* Windows Vista (Server 2008) or newer is required if the *release* build is used with liblzma/libsodium DLLs obtained from official or other sources (thus have unpatched minimal OS version numbers, more in [raddi-redist-windows](https://github.com/raddinet/raddi-redist-windows) repository).
* Windows 10 (any build beginning with 1507/2015 LTSB) is required for AArch64 (arm-64) architecture
   - **TBD** fully updated version (22H1?) might be required on ARM64 to run Win32 GUI client due to SQLite version

## Installer

*TBD*