# unpack-install-jammer

InstallJammer is a program which generates executable install files.

One InstallJammer project can generate installer executables for Microsoft
Windows, Linux and Unix based systems.

They are a slick implementation of a Windows style installer imported
to the Linux world.  They allow extensive customisability, the installer
can edit config files, restart services or and insert files as required
anywhere on the system.

If you are used to the Linux way of working downloading and running one
of these impenetrable binary blobs as root is bloody terrifying.

This script provides an alternative.

It will search through your binary install blob, identify and extract
the files buried within and drop them in a local directory. No running
as root required, the only thing that is executed is the Perl script which
lives up to Perl's reputation of easy inspection.

*WARNING*, this script worked for me, once, I developed it against
`Installer_LPCXpresso_8.2.2_650_Linux-x86` and my own generated installers.
Your mileage will probably vary.

## Usage

```
    ./extract.pl installer_blob
```

Files will be dropped in `./install_dir/`

See `./extract.pl --help` for fancy usage options.

Requires the following modules:
  * Modern::Perl
  * Compress::Raw::Lzma
  * Term::ProgressBar
  * Data::Dump

This should do it for a Debian based system:
```
    apt-get install libmodern-perl-perl libcompress-raw-lzma-perl libterm-progressbar-perl libdata-dump-perl
```

## Install Jammer

This project was developed completely without the endorsement or assistance
of the Install Jammer team.

Install Jammer was created by Damon Courtney, visible development ceased seven
years ago and he announced his intention to release the project to the users.

As far as I could discover, the source code has never been publicly published.
The Install Jammer releases consist of binary blobs and tcl files which allow
extensive customisation of the install process.

https://sourceforge.net/projects/installjammer/
https://github.com/damoncourtney/installjammer
