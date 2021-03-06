## git-replace-branch

This tool is written for github users who use an automated tool (such as
Doxygen) to generate documentation, and then publish the documentation on
github.io using a different branch on the same repository.

It is designed to automate the problem described
[here](http://stackoverflow.com/q/41113325/391161) without the need for
multiple clones.

The tool is entirely encapsulated in the file `git-replace-branch`, and the
purpose of this repository to merely to demonstrate its use.

Here is an example usage, using this repository. It assumes that there already
exists a local branch which tracks the correct remote branch.

    ./CreateContent.sh
    ./git-replace-branch Website gh-pages "Updating our website"

    # This part of the example will not work unless you fork my repository, but
    # it is illustrative for how you might write a script which leverages
    # git-replace-branch.
    git push origin gh-pages

Incidentally, the sample website associated with this repo is available
[here](https://hq6.github.io/git-replace-branch/). For more information about
the URL's associated with user repositories,
[this](https://help.github.com/articles/user-organization-and-project-pages/)
is a convenience reference.
