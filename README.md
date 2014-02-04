If you want to split subdirectories into a git submodule (or the other way around) while maintaining history of commits, you've come to the right spot.

:-D

Installation
===

    git clone https://github.com/apenwarr/git-subtree.git

    cd git-subtree
    sudo rsync -a ./git-subtree.sh /usr/local/bin/git-subtree

Or if you want the man pages and all

    make doc
    make install

Usage
===

Split a larger into smaller chunks:

    # Go into the project root
    cd ~/my-project

    # Create a branch which only contains commits for the children of 'foo'
    git subtree split --prefix=foo --branch=foo-only

    # Remove 'foo' from the project
    git rm -rf ./foo

    # Create a git repo for 'foo' (assuming we already created it on github)
    mkdir foo
    pushd foo
    git init
    git remote add origin git@github.com:my-user/new-project.git
    git pull ../ foo-only
    git push origin -u master
    popd

    # Add 'foo' as a git submodule to `my-project`
    git submodule add git@github.com:my-user/new-project.git foo

For detailed documentation (man page), please read `git-subtree.txt`.

Contact
===

Please don't contact me using github mail; it's slow, ugly, and worst of
all, redundant.

Email me instead at [apenwarr@gmail.com](apenwarr@gmail.com) and I'll be happy to
help.

Avery
