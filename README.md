# Dotfiles

This is a collection of dotfiles (no shit!).

It's built to work with [GNU Stow](https://www.gnu.org/software/stow/manual/stow.html). A useful introduction can be found [here](http://blog.xero.nu/managing_dotfiles_with_gnu_stow). Basically, running `stow my-directory` will symlink the files/folders in that directory into the prent directory. So by unpacking this repo in the home directory, running [_eg_] `stow spacemacs` from the repo root will symlink everything in the `spacemacs/` directory direct into the home directory. Easy. Note that stow works on _directories_, not individual files, which is why everything here is collected into discrete directories.
