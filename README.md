# Vim & Zsh Setting for Mac

Use Vundle to manage the plugin.

`PluginUpdate` 
`PluginClean`

## Installed Plugin

1. [Vim-airline](https://github.com/vim-airline/vim-airline)
2. [ctrlp.vim](https://github.com/kien/ctrlp.vim)
3. [nerdcommenter](https://github.com/scrooloose/nerdcommenter)
4. [auto-pairs](https://github.com/jiangmiao/auto-pairs)
5. [syntastic](https://github.com/vim-syntastic/syntastic)
6. [Vundle](https://github.com/VundleVim/Vundle.vim)

## Vundle Install and Setting

1. Introduction:

	Installation requires Git and triggers git clone for each configured repository to ~/.vim/bundle/ by default. Curl is required for search.
	
2. Set up Vundle:

	`$ git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim`
	
3. Configure Plugins:

	Put this at the top of your .vimrc to use Vundle. Remove plugins you don't need, they are for illustration purposes.
	
	~~~c
	set nocompatible              " be iMproved, required
	filetype off                  " required

	" set the runtime path to include Vundle and initialize
	set rtp+=~/.vim/bundle/Vundle.vim
	call vundle#begin()
	" alternatively, pass a path where Vundle should install plugins
	"call vundle#begin('~/some/path/here')

	" let Vundle manage Vundle, required 
	Plugin 'VundleVim/Vundle.vim'

	" The following are examples of different formats supported.
	" Keep Plugin commands between vundle#begin/end.
	" plugin on GitHub repo
	Plugin 'tpope/vim-fugitive'
	" plugin from http://vim-scripts.org/vim/scripts.html
	" Plugin 'L9'
	" Git plugin not hosted on GitHub
	Plugin 'git://git.wincent.com/command-t.git'
	" git repos on your local machine (i.e. when working on your own plugin)
	Plugin 'file:///home/gmarik/path/to/plugin'
	" The sparkup vim script is in a subdirectory of this repo called vim.
	" Pass the path to set the runtimepath properly.
	Plugin 'rstacruz/sparkup', {'rtp': 'vim/'}
	" Install L9 and avoid a Naming conflict if you've already installed a
	" different version somewhere else.
	" Plugin 'ascenator/L9', {'name': 'newL9'}

	" All of your Plugins must be added before the following line
	call vundle#end()            " required
	filetype plugin indent on    " required
	" To ignore plugin indent changes, instead use:
	"filetype plugin on
	"
	" Brief help
	" :PluginList       - lists configured plugins
	" :PluginInstall    - installs plugins; append `!` to update or just :PluginUpdate
	" :PluginSearch foo - searches for foo; append `!` to refresh local cache
	" :PluginClean      - confirms removal of unused plugins; 	append `!` to auto-approve removal
	"
	" see :h vundle for more details or wiki for FAQ
	" Put your non-Plugin stuff after this line
	
	~~~
	
4. Install Plugins:

	Launch vim and run : `PluginInstall`
	
## Vim Install in Mac

Use homebrew to manage package.

`brew update` : update homebrew first

`brew option vim` : see options,

`brew install vim`

`brew install vim --override-system-vim`

`brew install vim ----with-client-server` : This will enable the clipboard function of vim.  If you want X11 clipboard support, you need to install it with the --with-client-server option.

`brew uninstall vim` : to uninstall vim

`brew upgrade vim` : If you had Vim already installed with Homebrew (or if in the future you'd like to upgrade the Vim version).

One more thing you should do is to check your environment variables for those that might contain a full path to the system `vi/vim`, like EDITOR and update them to use the `/usr/local/bin/vim`.

Homebrew will install vim to `/usr/local/Cellar/vim/8.0.06`