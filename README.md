# dotfiles
A collection of my linux dotfiles

## Installing on a New System

Commit the alias to (`.zshrc`):<br>
(`alias config='/usr/bin/git --git-dir=$HOME/dotfiles/ --work-tree=$HOME'`)

Make sure source repo ignores file to clone to:<br>
(`echo "dotfiles" >> .gitignore`)

Clone dotfiles into a bare repo:<br>
(`git clone --bare <git-repo-url> $HOME/dotfiles`)

Define alias in current shell scope:<br>
(`alias config='/usr/bin/git --git-dir=$HOME/dotfiles/ --work-tree=$HOME'`)

Checkout the actual content from the bare repo:<br>
(`config checkout`)

You may need to either remove or abckup existing config files in $HOME:<br>

Se the flat showUntrackedFiles to no:<br>
(`config config --local status.showUntrackedFiles no`)

## Stuff to do

### Programs to install

* git
* zsh
* oh-my-zsh
* spaceship theme

## Dotfile Management
These dotfiles are based off the article:
https://www.atlassian.com/git/tutorials/dotfiles
