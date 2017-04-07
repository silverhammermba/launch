# launch #

Launch is a stupid-simple command line launcher. It is designed for users with a
terminal-centric workflow who occasionally want to run something with a GUI.

## Features ##

* stupid-simple. just type `launch cmd args ...`
* silences stdout/stderr e.g. so your shell doesn't get flooded with GTK
  warnings
* prints the new process's PID to stdout, so you can easily `ps` or `kill` it
* prints an error message if the command couldn't be launched
* _doesn't_ close stdin so you can pipe to it!

## Examples ##

Open a PDF with a relative path:

    $ launch evince docs/README.pdf

Pipe output into a GUI editor

    $ make 2>&1 | launch gedit -

## Building ##

Building is also stupid-simple. Just type

    $ make launch

Make's built-in rules will do the rest. If you want to customize the build,
define your own `CFLAGS` and `LDFLAGS`. `launch` is written in simple,
highly-portable C code. If building generates errors with your platform/compiler
please let me know.

### Packages ###

Currently available on:

* [AUR][1]
* [FreeBSD][2]

[1]: https://aur.archlinux.org/packages/launch-cmd/
[2]: https://bugs.freebsd.org/bugzilla/show_bug.cgi?id=218441
