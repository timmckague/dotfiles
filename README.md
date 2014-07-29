#dotfiles#
##bash##
All bash related files stored in bash folder

bash\_profile - just references bashrc, only there for mac functionality...?

path changes made in bash\_path

aliases in bash\_aliases

##vim##
for vim plugins and settings etc...
modelled after: http://mirnazim.org/writings/vim-plugins-i-use/


_add new submodules_:
$ git submodule add git://github.com/tpope/vim-fugitive.git bundle/fugitive

_run when adding new submodules_:
$ git submodule init && git submodule update

_update existing submodeles_:
$ git submodule foreach git pull


##screen##
makes bashrc work when in using screen although this could use some work...


##Setup##
git clone https://github.com/timmckague/dotfiles.git
mkdir old\_dotfiles
mv .bash\* old\_dotfiles/

ln -s dotfiles/bash/bashrc .bashrc
ln -s dotfiles/bash/bash\_profile .bash\_profile
ln -s dotfiles/tmux/tmux.conf .tmux.conf
ln -s dotfiles/vim/vimrc .vimrc
ln -s dotfiles/vim .vim

cd dotfiles
git submodule init && git submodule update


