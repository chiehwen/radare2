<pre>
    ____  ___  ___  ___ ____  ___    ____
   |  _ \/   \|   \/   \  _ \/ _ \  |__  \
   |    (  V  | |  ) V  |   (   _/   / __/ 
   |__\__|_|__|___/__|__|_\__|___|  |____|

                www.radare.org

                                  --pancake
</pre>

# Introduction

r2 is a rewrite from scratch of radare in order to provide
a set of libraries and tools to work with binary files

This is the rewrite of radare (1.x branch) to provide a
framework with a set of libraries and programs to work
with binary data.

Radare project started as a forensics tool, an scriptable
commandline hexadecimal editor able to open disk files,
but later support for analyzing binaries, disassembling
code, debugging programs, attaching to remove gdb servers, ..

radare2 is portable.

Architectures: x86, arm, mips, ppc, java, dalvik, arc, avr, bf, csr, dcpu16, m68k, msil, sh, sparc

File Formats: dex, elf, elf64, filesystem, java, fatmach0, mach0, mach0-64, MZ, PE, PE+, plan9, dyldcache

Operating Systems: Android, GNU/Linux, [Net|Free|Open]BSD, iOS, OSX, QNX, w32, w64, Solaris.

Bindings: Vala/Genie, Python, NodeJS, LUA, Go, Perl, Guile, php5, newlisp, Ruby, Java

# Dependencies

radare2 can be built without any special dependency, just
use make and get a working toolchain (gcc, clang, ..)

Optionally you can use libewf for loading EnCase disk images.

To build the bindings you need valabind, g++ and swig2.

# Install

Easiest way to install radare2 from git is by running
the following command:

    $ sys/install.sh

# Uninstall

In case of poluted filesystem you can uninstall current version or remove all previous installations:

    $ make uninstall
    $ make purge

# Bindings

All language bindings are under the r2-bindings directory.
You will need to install swig2 and valabind in order to
build the bindings for Python, LUA, etc..

APIs are defined in vapi files which are then translated
to swig interfaces, nodejs-ffi or other and then compiled.

Easiest way to install the python bindings is to run:

    $ sys/python.sh

If you want to use the NodeJS bindings just do:

    $ npm install radare2.js

You may like to specify the installed version of radare2:

    $ npm install radare2.js@0.9.2

# Tests

There is a test suite that can be retrieved by running:

    $ make tests

# Documentation

There is no formal documentation of r2 yet. Not all commands
are compatible with radare1, so the best way to learn how to
do stuff in r2 is by reading the examples from the web and
appending '?' to every command you are interested on.

Commands are small mnemonics of few characters and there is
some extra syntax sugar that makes the shell much more pleasant
for scripting and interacting with the apis.

# Webserver

radare2 comes with an embedded webserver that serves a pure
html/js interface that sends ajax queries to the core and
aims to implement an usable UI for phones, tablets and desktops.

    $ r2 -c=H /bin/ls

# Pointers

Website: http://www.radare.org/

IRC: irc.freenode.net #radare

Twitter: @radareorg
