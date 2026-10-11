# html2ps

This repository holds html2ps 1.0 beta7, released by Jan Kärrman on
2010-05-07, with the changes I need to render my own documentation. I keep
it for my personal use and don't maintain it. Issues and pull requests are
closed, and changes land here when I need them.

The original description of html2ps and its files is in [README](README).

## Changes

On top of the 1.0 beta7 release, which is the first commit:

* Remove the deprecated `$[` variable (Petr Písař, from Fedora).
* Fix the warnings and the removed `POSIX::tmpnam()` of Perl 5.22 and later
  (Todd Lewis, from Fedora), so that html2ps runs on current Perl.
* Paint the page background in colour mode when something is drawn on the
  page. html2ps used to paint it as it started a page, including a page that
  it then left out, which Ghostscript reports ("Page object was reserved for
  an Annotation destination, but no such page was drawn").
* Read the global configuration file from `/etc/html2psrc`, where Debian and
  Fedora install it.

## License

html2ps is licensed under the GNU General Public License, version 2 or later.

See [COPYING](COPYING).
