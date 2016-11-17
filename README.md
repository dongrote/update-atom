# update-atom
The Linux version of Atom does not have an update feature built into it. This
shell script solves that problem on Debian-based distributions.

Add it to your path and invoke with no parameters:

`$ update-atom`

The script will identify the currently installed version of Atom and compare it
with the latest available version of the editor. If the versions match, the
script aborts immediately. If the versions do not match it proceeds to download
the available version (assumed to be the latest) to
`$HOME/Downloads/atom-amd64.deb`, deleting a previously existing file if
present, and then proceeds to install the downloaded package; sudo privileges
are required.

Behavior is undefined if Atom is not already installed.
