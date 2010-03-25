post-checkout
  Everytime you checkout a branch, this hook will scan the repository for
  any .pyc files that do not have a matching .py file. That is useful when
  switching between branches where some Python code has been removed.
  Presumably, you have Git configured to ignore .pyc files, but that means
  that Git can leave a .pyc file behind when the .py file is moved or
  deleted, and that can lead to mysterious errors when the Python
  interpreter continues to use the old .pyc file.

One way to use a git hook from this repo in another project would be to
symlink the relevant file::

    ln -s git_hooks/post-checkout REPO/.git/hooks/
