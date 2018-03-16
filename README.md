# Dotfiles

This is a collection of dotfiles (no shit!).

It's built to work with [GNU Stow](https://www.gnu.org/software/stow/manual/stow.html). A useful introduction can be found [here](http://blog.xero.nu/managing_dotfiles_with_gnu_stow). Basically, running `stow my-directory` will symlink the files/folders in that directory into the prent directory. So by unpacking this repo in the home directory, running [_eg_] `stow spacemacs` from the repo root will symlink everything in the `spacemacs/` directory direct into the home directory. Easy. Note that stow works on _directories_, not individual files, which is why everything here is collected into discrete directories.

## "xresources"

I've grouped all functionality related to my Linux environment here. So there should be configuration for:

- [ ] A tiling window manager ([i3]()). i3 seems good, and it has good explanatory videos.
- [ ] An application launcher ([rofi]()) - Once in a window manager, there's likely to be minor difficulties actually opening anything that isn't a terminal without this, so this is a necessity.
- [ ] A terminal ([URxvt]()). Doesn't really matter which terminal, but URxvt allows config via the `.Xresources` file, which is nice and easy.
- [ ] An application that allows desktop wallpapers ([Feh]()). Whatever.


### Installs [possibly] needed:

The key install:

```
sudo pacman -S i3-gaps # tiling window manager (fork, allows gaps)
```

Want a better theme as well, so install the Arc theme via pacman, and
then update the .config/gtk-3.0/settings.ini to use Arc-Dark, and update
the font to Roboto while you're at it.

Install geany and load the Nord theme (using Emacs most of the time, but
a fast lightweight editor is nice as well).

Possibly these, though there is the thing that you can't pad the bar, wtf just let me add some whitespace:
```
sudo pacman -S i3status # status bar for i3
sudo pacman -S i3blocks # use the blocks application to pipe stuff into the i3 bar
```

Anyway,
```
sudo pacman -S i3lock # lockscreen for i3
sudo pacman -S rofi # application launcher
sudo pacman -S compton # compositor (for shadows)
sudo pacman -S rxvt-unicode # terminal (URxvt, so can set colours etc in Xresources file)
sudo pacman -S feh # tiny image editor that allows setting wallpapers
```
