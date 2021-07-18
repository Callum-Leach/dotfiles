# dotfiles
A collection of my linux dotfiles

## Installing on a New System

### Auto-Install Script

`curl -Lks http://bit.do/fPkTe | /bin/bash`

### Manual

Commit the alias to (`.zshrc`):<br>
`alias config='/usr/bin/git --git-dir=$HOME/dotfiles/ --work-tree=$HOME'`

Make sure source repo ignores file to clone to:<br>
`echo "dotfiles" >> .gitignore`

Clone dotfiles into a bare repo:<br>
`git clone --bare <git-repo-url> $HOME/dotfiles`

Define alias in current shell scope:<br>
`alias config='/usr/bin/git --git-dir=$HOME/dotfiles/ --work-tree=$HOME'`

Checkout the actual content from the bare repo:<br>
`config checkout`

You may need to either remove or abckup existing config files in $HOME:<br>

Se the flat showUntrackedFiles to no:<br>
`config config --local status.showUntrackedFiles no`



## Stuff to do

### Programs to install

* git
* zsh: `sudo apt install zsh`
* [oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh)
* [spaceship prompt](https://github.com/denysdovhan/spaceship-prompt)
* [polybar wireguard](https://github.com/polybar/polybar-scripts/tree/master/polybar-scripts/vpn-wireguard-wg)
* [latex-vim](https://castel.dev/post/lecture-notes-1/)
* [mutt-wizard](https://github.com/LukeSmithxyz/mutt-wizard)
* [bspwm]
* [sxhxd]
* [pywal]
#### Polybar Scripts
* [polybar-gmail](https://github.com/crabvk/polybar-gmail)

To get wireguard polybar working, I had to change permissions of wireguard folder using:
`sudo chown callumleach /etc/wireguard`. I want to change this, bad practice.

## Dotfile Management
These dotfiles are based off the article:
https://www.atlassian.com/git/tutorials/dotfiles
