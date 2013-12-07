This repository is for easily setting-up my preferred command-line environment 
on any machine.

# Installation

    git clone git://github.com/red-crown/dotfiles.git ~/.dotfiles

# Updating
Ensure submodules are initialized and updated.

    $ cd ~/.dotfiles
    $ git submodule init
    $ git submodule update

It is also possible to use `git pull` to update the submodules.

    $ cd ~/.dotfiles
    $ git submodule foreach git pull origin master

Vundle managed Vim bundles maybe updated from the command line via

    $ vim +BundleInstall +qall

# Setup
You can setup these settings by either running the included installation script
or by installing each manually.

## Automatically

    $ cd ~/.dotfiles && ./install

This will automatically create all the necessary symlinks based on the os.

## Manually
### bash

### Vim
For Vim configuration and use, create the following symlinks:

    ln -s  ~/.dotfiles/vim        ~/.vim
    ln -s  ~/.dotfiles/vim/vimrc  ~/.vimrc

To install Vim bundles, which are managed via Vundle, via the command line run

    vim +Bundleinstall +qall

From inside of Vim run

    :BundleInstall

If this is the first time setting up Vim on the machine, it will be necessary 
to install Vundle itself, prior to the bundles.

    git clone https://github.com/gmarik/vundle.git ~/.vim/bundle/vundle

### bash
To set up basic settings in bash:

    $ ln -s  ~/.dotfiles/bash/bash_profile   ~/.bash_profile
    $ ln -s  ~/.dotfiles/bash/bashrc         ~/.bashrc
    $ ln -s  ~/.dotfiles/bash/bash_aliases   ~/.bash_aliases
    $ ln -s  ~/.dotfiles/bash/bash_history   ~/.bash_history

