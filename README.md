# GNU Libiconv for C++ Plus
## This is package 'libiconv' for The C++ Plus Project


This library is used for the GNU Libiconv dependency of The C++ Plus Project

# Version
GNU Libiconv 1.17

# Build
You can use CMake or GNU Make to compile cppp.libiconv

## CMake
CMake compilation can be used for all platforms in theory. We recommend using CMake to compile
### Dependencies
* CMake
  + Mandatory.
    You must have CMake 3.1 or later.
  + CMake Homepage:
    https://cmake.org/
  + Download:
    https://cmake.org/download/
* A C runtime, compiler, linker, etc.
  + Mandatory.
  + GCC Homepage:
    https://gcc.gnu.org/
  + Download:
    https://ftp.gnu.org/gnu/gcc/
  + MSVC Homepage:
    https://visualstudio.microsoft.com/
  + Download:
    https://visualstudio.microsoft.com/downloads/
* A 'make' utility **(You can use MSBuild on Windows platform)**.
  + Mandatory **on Non-Windows platform**.
    Either the platform's native 'make' (for in-tree builds only),
    or GNU Make 3.79.1 or newer.
  + GNU Make Homepage:
    https://www.gnu.org/software/make/
  + Download:
    https://ftp.gnu.org/gnu/make/

### Windows MSVC
```shell
mkdir build
cd build
cmake ..
msbuild cppp.libiconv.sln
```
### Other Platforms
```shell
mkdir build
cd build
cmake ..
make
# You can use 'make -j$(nproc) to enable multi-core compilation'
```
## GNU Make
### Dependencies
* A C runtime, compiler, linker, etc.
  + Mandatory.
    Either the platform's native 'cc', or GCC 3.1 or newer.
  + GCC Homepage:
    https://gcc.gnu.org/
  + Download:
    https://ftp.gnu.org/gnu/gcc/

* A 'make' utility.
  + Mandatory.
    Either the platform's native 'make' (for in-tree builds only),
    or GNU Make 3.79.1 or newer.
  + GNU Make Homepage:
    https://www.gnu.org/software/make/
  + Download:
    https://ftp.gnu.org/gnu/make/

* A shell
  + Mandatory.
    Either the platform's native 'sh', or Bash.
  + Homepage:
    https://www.gnu.org/software/bash/
  + Download:
    https://ftp.gnu.org/gnu/bash/

* Core POSIX utilities,
  + including: **[ basename cat chgrp chmod chown cp dd echo expand expr
    false hostname install kill ln ls md5sum mkdir mkfifo
    mknod mv printenv pwd rm rmdir sleep sort tee test touch
    true uname**
  + Mandatory.
    Either the platform's native utilities, or GNU coreutils.
  + Homepage:
    https://www.gnu.org/software/coreutils/
  + Download:
    https://ftp.gnu.org/gnu/coreutils/

* The comparison utilities 'cmp' and 'diff'.
  + Mandatory.
    Either the platform's native utilities, or GNU diffutils.
  + Homepage:
    https://www.gnu.org/software/diffutils/
  + Download:
    https://ftp.gnu.org/gnu/diffutils/

* Grep.
  + Mandatory.
    Either the platform's native grep, or GNU grep.
  + Homepage:
    https://www.gnu.org/software/grep/
  + Download:
    https://ftp.gnu.org/gnu/grep/

* Awk.
  + Mandatory.
    Either the platform's native awk, mawk, or nawk, or GNU awk.
  + Homepage:
    https://www.gnu.org/software/gawk/
  + Download:
    https://ftp.gnu.org/gnu/gawk/
### Start Build
```shell
chmod +x configure
./configure --prefix=$(pwd)/build --enable-shared --enable-static --enable-relocatable
make
make install
# You can use 'make -j$(nproc) to enable multi-core compilation'
```
### Configure Usage
```
`configure' configures libiconv 1.17 to adapt to many kinds of systems.      

Usage: configure [OPTION]... [VAR=VALUE]...

To assign environment variables (e.g., CC, CFLAGS...), specify them as       
VAR=VALUE.  See below for descriptions of some of the useful variables.      

Defaults for the options are specified in brackets.

Configuration:
  -h, --help              display this help and exit
      --help=short        display options specific to this package
      --help=recursive    display the short help of all the included packages
  -V, --version           display version information and exit
  -q, --quiet, --silent   do not print `checking ...' messages
      --cache-file=FILE   cache test results in FILE [disabled]
  -C, --config-cache      alias for `--cache-file=config.cache'
  -n, --no-create         do not create output files
      --srcdir=DIR        find the sources in DIR [configure dir or `..']

Installation directories:
  --prefix=PREFIX         install architecture-independent files in PREFIX
                          [/usr/local]
  --exec-prefix=EPREFIX   install architecture-dependent files in EPREFIX
                          [PREFIX]

By default, `make install' will install all the files in
`/usr/local/bin', `/usr/local/lib' etc.  You can specify
an installation prefix other than `/usr/local' using `--prefix',
for instance `--prefix=$HOME'.

For better control, use the options below.

Fine tuning of the installation directories:
  --bindir=DIR            user executables [EPREFIX/bin]
  --sbindir=DIR           system admin executables [EPREFIX/sbin]
  --libexecdir=DIR        program executables [EPREFIX/libexec]
  --sysconfdir=DIR        read-only single-machine data [PREFIX/etc]
  --sharedstatedir=DIR    modifiable architecture-independent data [PREFIX/com]
  --localstatedir=DIR     modifiable single-machine data [PREFIX/var]
  --runstatedir=DIR       modifiable per-process data [LOCALSTATEDIR/run]
  --libdir=DIR            object code libraries [EPREFIX/lib]
  --includedir=DIR        C header files [PREFIX/include]
  --oldincludedir=DIR     C header files for non-gcc [/usr/include]
  --datarootdir=DIR       read-only arch.-independent data root [PREFIX/share]
  --datadir=DIR           read-only architecture-independent data [DATAROOTDIR]
  --infodir=DIR           info documentation [DATAROOTDIR/info]
  --localedir=DIR         locale-dependent data [DATAROOTDIR/locale]
  --mandir=DIR            man documentation [DATAROOTDIR/man]
  --docdir=DIR            documentation root [DATAROOTDIR/doc/libiconv]
  --htmldir=DIR           html documentation [DOCDIR]
  --dvidir=DIR            dvi documentation [DOCDIR]
  --pdfdir=DIR            pdf documentation [DOCDIR]
  --psdir=DIR             ps documentation [DOCDIR]

Program names:
  --program-prefix=PREFIX            prepend PREFIX to installed program names
  --program-suffix=SUFFIX            append SUFFIX to installed program names
  --program-transform-name=PROGRAM   run sed PROGRAM on installed program names

System types:
  --build=BUILD     configure for building on BUILD [guessed]
  --host=HOST       cross-compile to build programs to run on HOST [BUILD]

Optional Features:
  --disable-option-checking  ignore unrecognized --enable/--with options
  --disable-FEATURE       do not include FEATURE (same as --enable-FEATURE=no)
  --enable-FEATURE[=ARG]  include FEATURE [ARG=yes]
  --enable-silent-rules   less verbose build output (undo: "make V=1")
  --disable-silent-rules  verbose build output (undo: "make V=0")
  --enable-dependency-tracking
                          do not reject slow dependency extractors
  --disable-dependency-tracking
                          speeds up one-time build
  --disable-largefile     omit support for large files
  --disable-year2038      omit support for timestamps past the year 2038
  --enable-static[=PKGS]  build static libraries [default=no]
  --enable-shared[=PKGS]  build shared libraries [default=yes]
  --enable-fast-install[=PKGS]
                          optimize for fast installation [default=yes]
  --disable-libtool-lock  avoid locking (might break parallel builds)
  --enable-relocatable    install a package that can be moved in the file
                          system
  --enable-extra-encodings
                          add support for a few rarely used encodings
  --disable-rpath         do not hardcode runtime library paths
  --disable-nls           do not use Native Language Support
  --enable-cross-guesses={conservative|risky}
                          specify policy for cross-compilation guesses

Optional Packages:
  --with-PACKAGE[=ARG]    use PACKAGE [ARG=yes]
  --without-PACKAGE       do not use PACKAGE (same as --with-PACKAGE=no)
  --with-pic[=PKGS]       try to use only PIC/non-PIC objects [default=use
                          both]
  --with-aix-soname=aix|svr4|both
                          shared library versioning (aka "SONAME") variant to
                          provide on AIX, [default=aix].
  --with-gnu-ld           assume the C compiler uses GNU ld [default=no]
  --with-sysroot[=DIR]    Search for dependent libraries within DIR (or the
                          compiler's sysroot if not specified).
  --with-gnu-ld           assume the C compiler uses GNU ld [default=no]
  --with-libiconv-prefix[=DIR]  search for libiconv in DIR/include and DIR/lib
  --without-libiconv-prefix     don't search for libiconv in includedir and libdir
  --with-libintl-prefix[=DIR]  search for libintl in DIR/include and DIR/lib
  --without-libintl-prefix     don't search for libintl in includedir and libdir

Some influential environment variables:
  CC          C compiler command
  CFLAGS      C compiler flags
  LDFLAGS     linker flags, e.g. -L<lib dir> if you have libraries in a
              nonstandard directory <lib dir>
  LIBS        libraries to pass to the linker, e.g. -l<library>
  CPPFLAGS    (Objective) C/C++ preprocessor flags, e.g. -I<include dir> if
              you have headers in a nonstandard directory <include dir>
  CPP         C preprocessor
  LT_SYS_LIBRARY_PATH
              User-defined run-time library search path.

Use these variables to override the choices made by `configure' or to help
it to find libraries and programs with nonstandard names/locations.

Report bugs to the package provider.
```

# Licence
GNU General Public License 3.29