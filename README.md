
About Meld
==========

Meld is a visual diff and merge tool targeted at developers. Meld helps you
compare files, directories, and version controlled projects. It provides
two- and three-way comparison of both files and directories, and supports
many version control systems including Git, Mercurial, Bazaar, CVS and Subversion.

Meld helps you review code changes, understand patches, and makes enormous
merge conflicts slightly less painful.

Meld is licensed under the GPL v2 or later.


Requirements
------------

* Python 3.6
* pycairo (Python3 bindings for cairo without GObject layer)
* PyGObject 3.30 (Python3 bindings for GObject introspection)
* gsettings-desktop-schemas

And following packages with GObject introspection:

* GLib 2.36
* Pango
* PangoCairo
* GTK+ 3.20
* GtkSourceView 4.0


Build requirements
------------------

* Python 3.6
* Meson 0.48
* Ninja
* gettext
* GLib 2.36 and its development utilities such as `glib-compile-schemas`

For Windows build requirements, see `mingw-common` section `.gitlab-ci.yml`


Running
-------

You *do not* need to build Meld in order to run it. Meld can be run directly
from this source directory by running:

```sh
$ bin/meld
```

Unix users should get Meld from their distribution package manager, or from
[Flathub](https://flathub.org/).

Windows users should download the provided MSIs on the
[Meld home page](https://meld.app/).

OSX users can install Meld using Homebrew (or Macports, Fink, etc.), or there
are unofficial native builds available from the
[Meld for OSX](https://yousseb.github.io/meld/) project.


Building
--------

Meld uses [meson](https://mesonbuild.com/) build system. Use the following
commands to build Meld from the source directory:

```sh
$ meson _build
$ cd _build
$ ninja
```

You can then install Meld system-wide by running:

```sh
$ ninja install
```

A Windows installer can be built with command

```powershell
C:\Python34\python.exe setup_win32.py bdist_msi
```

which will create the file `dist/Meld-VERSION-ARCH.msi`.


Developing
----------

It's easy to get started developing Meld. From a git checkout, just run
`bin/meld`.

We also support development using Flatpak via GNOME Builder. At the Builder
"Clone..." dialog, enter https://gitlab.gnome.org/GNOME/meld.git, and the
default build + run development flow using Flatpak should work.


Contributing
------------

Meld uses GNOME's GitLab to track bugs, and user questions and development
discussions happen on the Meld mailing list. The development team is small,
and new contributors are always welcome!

List of issues: https://gitlab.gnome.org/GNOME/meld/issues

Support forum:  https://discourse.gnome.org/tag/meld



Links
-----

Home page:      https://meld.app/

Documentation:  https://meld.app/help/

Wiki:           https://wiki.gnome.org/Apps/Meld
