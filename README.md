# git-subtree

git-subtree allows subprojects to be included within a sub-directory of a main project, optionally including the sub-project's entire history.

## Installation

Choose **one** of the following ways to install git-subtree:

1. Copy the file `git-subtree.sh` to where all other git scripts are stored.
1. Run `install.sh` in a Git-enabled shell (that's "Git Bash" on Windows).
1. Run `make install` in a Cygwin-enabled shell.

Any *one* of these actions makes the `git subtree` command available (note: space instead of dash).

To additionally install the man page:

    make doc
    cp git-subtree.1 /usr/share/man/man1/


## Usage

See `git-subtree.txt` for details.

## Known issues

See `todo`.

## License

You may use this software under the terms of the GNU General Public License (GPL), Version 2.

See `COPYING`.

## Credits

Originally authored by Avery Pennarun, <http://apenwarr.ca/log>

Please do not contact the author using github mail. Instead, <mailto:apenwarr@gmail.com>
