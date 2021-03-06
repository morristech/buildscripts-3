Ricochet Build Scripts
----------------------

These are the scripts and instructions used to build distribution binaries for Ricochet, for various platforms.

If you don't know what Ricochet is or you're trying to find pre-built binaries, you're probably more interested in the [main repository](https://github.com/ricochet-im/ricochet) or [website](https://ricochet.im/).

If you want to build your own Ricochet for local use, there are general [build instructions](https://github.com/ricochet-im/ricochet/blob/master/BUILDING.md). These scripts might still be useful to you, because they take care of all dependencies and create redistributable binaries.

Platforms
---------

*linux-static* creates a portable Linux binary that statically links all non-standard libraries. It's intended to be a best-effort at creating one binary that can run unmodified on most modern Linux systems. The scripts are tailored to build from a Debian stable machine, but the resulting binaries should be compatible with many distributions.

*mingw-cross* cross-compiles 32bit Windows binaries using the MinGW-w64 toolchain. It's compatible with mingw packages included in many distributions. This is the recommended way to build for Windows machines.

*mingw* builds from a MSYS2/MinGW-w64 environment on Windows. This can be difficult to get working correctly, so cross-compilation is often a better choice.

*osx* builds a MacOS self-contained .app and packages it into .dmg. This requires MacOS with xcode and commandline tools.

Building
--------

See individual directories for build instructions. Generally, set `MAKEOPTS=-j6`, run `./platform/build-deps.sh`, checkout the commit you want to `src/ricochet`, and run `./platform/build.sh`

