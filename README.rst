One way to use a git hook from this repo in another project would be to
symlink the relevant file::

    ln -s git_hooks/post-checkout REPO/.git/hooks/
