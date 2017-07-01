# Vim & Zsh Setting for Mac

Use Vundle to manage the plugin.

`PluginUpdate` 
`PluginClean`

[Markdown GitHub Editor](https://jbt.github.io/markdown-editor/#bVNBbtswELzzFVs4gO3GltpremqTpgkQA0WTnoICoUVSpC1yBXJlJyn69y4pw84hgAnJ5HBmd2Y1gdkPRzfDenndyR1GreawknGrcB/gu3KEUYhvMrkGhqTN0IHRkoaooXOJLoSAj3BJsTu/hxouveInISS500BWg3GdPkGsM3QCHv4xvLGISR8vynQqASPcPKzuMsdVlC3IoEBF7EEWbnCBb1kdy+0OpQJHGXydDxsMpAMlkHyeqfk0lLp+/7qDhPCCAzQyQLIZkQmTEOJ26iEgtIgKJME+OnKhZQLfM2mdcZ2OQPqZFpmlxYJhCfSabMYycUy6M5UQd4jbBZeb/fpQ/DKI+bGWcXy8CvGV28pdTFMh4cqV/gAX55/Z4aenp43cydRE15M4m5khNOQwzOZ/BcDZbKrcbjqvLPluNr0F6VmMt6rp/Iv4x4vvC/FgXQL+PWKAMfA/M0vUp4u6bh3ZYV016OvNmmp/8H6pS/zz3GKnCbisbcA9OAO3U45p/Slus6NUSt7n8rld8ZPTSTmNVazgCnFdMsvyj7krGFlHdRb3UTGmiPcRN7qhVGfcQb2eL8BE9LC3rrEiZ+dC6l2U2YIsw4anRdEozll+ewGXo/Kc/QjjTIhBjfS5xMlkAvc0GJNHWmUOL7e6EI0D/Xi0wNG7Nr05f/s+52jjaXZ7GRMPQ2G85JZWLsY3necufdmqgqZ6vJwblHtdWkkvXP/z0rrWdryIax1NKYzH7WqTjpwJDe15lr0MTjapwtiWvfqIrnU4SI30cDzJc8ufBw7UD1QmENYdNttU5DZpqbTpJOl3HVEybLGVrj7hRpX21fV9pkYDSpI82s1zY3ixIn+MSfwH)

[MarkDown emoji](https://gist.github.com/rxaviers/7360908) :+1: :sunny: :tada:

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
	
	```bash
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
	```
	
4. Install Plugins:

	Launch vim and run : `PluginInstall`
	
## Vim Install in Mac

- Use [homebrew](http://www.bigfastblog.com/homebrew-intro-to-the-mac-os-x-package-installer) to manage package.

	`brew update` : update homebrew first

	`brew options vim` : see options,

	`brew install vim`

	`brew install vim --override-system-vim` :Dangerous

	`brew install vim ----with-client-server` : This will enable the clipboard function of vim.  If you want X11 clipboard support, you need to install it with the --with-client-server option. 
:**Dangerous**!! will install a non Mac-compatable version, which make the system clipboard not accessed to vim.

	`brew uninstall vim` : to uninstall vim

	`brew upgrade vim` : If you had Vim already installed with Homebrew (or if in the future you'd like to upgrade the Vim version).

	One more thing you should do is to check your environment variables for those that might contain a full path to the system `vi/vim`, like EDITOR and update them to use the `/usr/local/bin/vim`.

- Homebrew will install vim to `/usr/local/Cellar/vim/8.0.06`

- If you have two versions of one software, like vim 8.0 and vim7.0. And f you want to keep both, you'll need to change your `$PATH` environment variable so that **the location of the new version appears before the location of the old version**. Do this by editing `~/.bash_profile` or `~/.zshrc`.

## Problem

1. Access system clipboard of Mac:

	`vim --version | grep clipboard` : check current vim support clipboard and -xterm_clipboard. Use MacOS X (unix) version, or system clipboard may not be used!!!!!!
	
	```
	➜  ~ vim --version
	VIM - Vi IMproved 8.0 (2016 Sep 12, compiled Jun 24 2017 12:45:56)
	➜ MacOS X (unix) version
	Included patches: 1-666
	➜ Compiled by Homebrew
  	```
	
	Iterm2 : 
	
	Select Copy to pasteboad on selection
	
	select Applications in terminal may access clipboard
	
	in `.vimrc` :
	
	`set clipboard=unnamed `   "set copy to system clipboard
	

[Ref1 Not Resolevd](http://vim.wikia.com/wiki/Accessing_the_system_clipboard) 

[Ref2 Not Resolevd](http://www.markcampbell.me/2016/04/12/setting-up-yank-to-clipboard-on-a-mac-with-vim.html)
	
2. "backspace wont delete in insert mode

	`set backspace=indent,eol,start`
	
3. Disable automatic comm: 
	
	`autocmd BufNewFile,BufRead * setlocal formatoptions-=cro`

	to check flag
	`:set formatoptions?`
	
	Automatically insert the current comment leader after hitting 'o' or 'O' in Normal mode.ent insertion
	"autocmd FileType * setlocal
	"formatoptions-=c formatoptions-=r formatoptions-=o
	"set formatoptions-=cro
	"I've got set formatoptions-=cro in my vimrc, but for some reason it doesn't stick. Problem is C file plugin in VIM. Since file plugin is loaded after loading .vimrc, the settings in .vimrc are overwritten.
