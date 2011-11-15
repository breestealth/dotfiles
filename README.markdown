This repository holds my Vim configuration so that I can clone it to other machines
easily. Eventually it will also house things like my zsh rc file.

Installation:

    git clone git://github.com/zan5hin/dotfiles.git ~/.dotfiles

Create the following symlinks:

    ln -s ~/.dotfiles/vimrc ~/.vimrc
    ln -s ~/.dotfiles/vim ~/.vim

Vim's backup and swap files are stored in `~/.tmp`, so that directory must exist. To be sure run:

    mkdir ~/.tmp

Recipe for cloning to a machine, including git submodule init and update:

    cd ~
    git clone http://github.com/zan5hin/dotfiles.git ~/.dotfiles
    ln -s ~/.dotfiles/vimrc ~/.vimrc
    ln -s ~/.dotfiles/vim ~/.vim
    mkdir ~/.tmp
    cd ~/.dotfiles
    git submodule init
    git submodule update

Upgrade a single bundle:

    cd ~/.dotfiles/vim/bundle/fugitive
    git pull origin master

Upgrade all bundles:

    cd ~/.dotfiles
    git submodule foreach git pull origin master

