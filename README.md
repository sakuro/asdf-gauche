[![Build Status](https://travis-ci.org/sakuro/asdf-gauche.svg?branch=master)](https://travis-ci.org/sakuro/asdf-gauche)

[Gauche](http://practical-scheme.net/gauche/index.html) plugin for
asdf version manager

# Install

```bash
asdf plugin-add gauche https://github.com/sakuro/asdf-gauche.git
```

# Use

Check [asdf](https://github.com/asdf-vm/asdf) readme for instructions
on how to install & manage versions of Gauche.

# Note

## SLIB

If you have [SLIB](https://people.csail.mit.edu/jaffer/SLIB) installed
in one of the following directories:

- `$(brew --prefix)/lib/slib` (only if you are using Homebrew[*])
- `/usr/local/slib`
- `/usr/local/lib/slib`
- `/opt/local/lib/slib`

the interpreter automatically detects where it is and sets
`SCHEME_LIBRARY_PATH` accordingly.

[*]: The formula of slib is in [sakuro/formulae](https://github.com/sakuro/homebrew-formulae)

```scheme
(sys-getenv "SCHEME_LIBRARY_PATH") #; "..path..to../slib"
(use slib)
(require 'factor) #; #t
(factor 120) #; (2 2 2 3 5)
```

## Source Location

At the time of this writing,
[sourceforge.net](https://sourceforge.net/projects/gauche/files/Gauche/)
is used for listing versions and fetching source tarballs because tarballs on
[GitHub releases](https://github.com/shirok/Gauche/releases) require
additional tool(autoconf) to generate the configure script.
