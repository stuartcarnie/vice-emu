# VICE

This is a fork of VICE, with a patch to add new UI to the _Video Settings_

# Building

## Mac OS X
From fresh clone, configure your environment.  Run from within `vice` directory

* `./autogen.sh`

### Configure build type
Release build:

* `./configure --with-cocoa`

Debug build:

* `env CFLAGS="-g -O0" OBJCFLAGS="-g -O3" configure --with-cocoa`

### Build
Build x64 and generate app bundle

* `make x64 && src/arch/unix/macosx/make-bindist.sh -t . -v 2.5 -e x64 -b`

### Run
Run from command line

* `./vice-macosx-cocoa-x86_64-2.5/x64.app/Contents/MacOS/x64`