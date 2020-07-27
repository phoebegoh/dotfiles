# dotfiles
All my dotfiles saved forevermore

# Setup
(See: https://github.com/anandpiyer/.dotfiles/tree/master/.dotfiles)
```
git init --bare $HOME/.dotfiles
alias dotfiles='git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME'
dotfiles remote add origin https://github.com/phoebegoh/dotfiles.git
dotfiles config --local status.showUntrackedFiles no
```

# Restore
```
   git clone --separate-git-dir=$HOME/.dotfiles https://github.com/phoebegoh/dotfiles.git $HOME/dotfiles-tmp
   rsync --recursive --verbose --exclude '.git' dotfiles-tmp/ $HOME/
   rm --recursive $HOME/dotfiles-tmp
```
## Notes about specific apps
iterm2: Load preferences from custom folder or URL.

# Usage
```dotfiles status
dotfiles add .somenewdotfile
dotfiles commit -m "added .somenewdotfile"
dotfiles push
```
