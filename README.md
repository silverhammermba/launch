## launch ##

Launch is a stupid-simple command line launcher. Designed for users with a
terminal-centric workflow but who occasionally want to run something with a GUI.

### Features ###

* stupid-simple. just type `launch cmd args ...`
* silences stdout/stderr e.g. so your shell doesn't get flooded with GTK warnings
* prints the new process's PID to stdout, so you can easily `ps` or `kill` it
* prints an error message if the command couldn't be launched
* _doesn't_ close stdin so you can pipe to it!

### Examples ###

Open a PDF with a relative path:

    $ launch evince docs/README.pdf

Pipe output into a GUI editor

    $ make 2>&1 | launch gedit -

### Building ###

Building is also stupid-simple. Just type

    make launch

Make's implicit rules will do the rest. If you want to customize the build,
define your own `CFLAGS` and `LDFLAGS`.

### Packages ###

Currently only available on Arch via the [AUR][1].

[1]: https://aur.archlinux.org/packages/launch-cmd/
