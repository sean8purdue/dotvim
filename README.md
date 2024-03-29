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
7. [tagbar](https://github.com/majutsushi/tagbar)
8. [easymotion](https://github.com/easymotion/vim-easymotion)
9. [autotag](https://github.com/craigemery/vim-autotag)
10. [sneak](https://github.com/justinmk/vim-sneak)

## Update

- 090817
	- Install Tagbar plugin   
  	Set map key for `Tagbar` troggle, revise map for `Ctrlp+tags`
  	- Install `easymotion` and map `goto word`
  	- Install `autotag` plugin
  	- Map forward key for `ctags`

```
nmap <leader>f :CtrlPTag<CR>
nmap <leader>g :CtrlP ..<CR>

" Set Tagbar
nnoremap <silent> <leader>b :TagbarToggle<CR>

" Ease Motion
" Move to word map  <Leader>w <Plug>(easymotion-bd-w)
nmap <Leader>w <Plug>(easymotion-overwin-w)

 " Set ctags
nnoremap <C-f> :tag<CR>

```



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

### 1 Access system clipboard of Mac:

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

### 2 backspace wont delete in insert mode

#### - If backspace won't delete in vim, then add the belowing line in `.vimrc`

	`set backspace=indent,eol,start`
	
#### - Fix the backspace key won't delete in zsh vi mode

add this line in `.zshrc`

`bindkey "^?" backward-delete-char`

#### - map `<CTRL>w` to backward kill word in insert mode of zsh vi mode

add this line in `.zshrc`

`bindkey "^W" backward-kill-word`

<ref>(https://superuser.com/questions/476532/how-can-i-make-zshs-vi-mode-behave-more-like-bashs-vi-mode)
	
### 3 Disable automatic comm: 
	
	`autocmd BufNewFile,BufRead * setlocal formatoptions-=cro`

	to check flag
	`:set formatoptions?`
	
	Automatically insert the current comment leader after hitting 'o' or 'O' in Normal mode.ent insertion
	"autocmd FileType * setlocal
	"formatoptions-=c formatoptions-=r formatoptions-=o
	"set formatoptions-=cro
	"I've got set formatoptions-=cro in my vimrc, but for some reason it doesn't stick. Problem is C file plugin in VIM. Since file plugin is loaded after loading .vimrc, the settings in .vimrc are overwritten.
	
### 4 Heighlight all search patterns and Map <CR> to clear last search highlighting
	
	`set hlsearch` 
	
	`nnoremap <CR> :noh<CR>`    
	   
	**!!!! Dangerous!!** Map \<ESC> May course errors and unexpected behaviours
	

### 5 kill the lag in vi mode of zsh
By default, there is a 0.4 second delay after you hit the <ESC> key and when the mode change is registered. This results in a very jarring and frustrating transition between modes. Let's reduce this delay to 0.1 seconds.

~~~
export KEYTIMEOUT=1
~~~

This can result in issues with other terminal commands that depended on this delay. If you have issues try raising the delay.

### 6 Ctrlp 

* Clear Cache

In vim type `:CtrlPClearCache`, or   
in ctrl-p mode already: hit <F5>. (Sometime not work)

Will clear the cache for **current vim working directory** only!!

Did you press <F5> in CtrlP or run `:CtrlPClearAllCaches` to clear the cache? If you want to be sure, delete the `.cache/ctrlp` dir in your home dir will delete cache for all directories.

* Exclude files and directories using Vim's `wildignore` and CtrlP's own `g:ctrlp_custom_ignore`:


```vim
    set wildignore+=*/tmp/*,*.so,*.swp,*.zip     " MacOSX/Linux
    set wildignore+=*\\tmp\\*,*.swp,*.zip,*.exe  " Windows

    let g:ctrlp_custom_ignore = '\v[\/]\.(git|hg|svn)$'
    let g:ctrlp_custom_ignore = {
      \ 'dir':  '\v[\/]\.(git|hg|svn)$',
      \ 'file': '\v\.(exe|so|dll)$',
      \ 'link': 'some_bad_symbolic_links',
      \ }
```

### 7 Z

* Clear Cache

delete the `.z` file in the root directory. `.z` file have the browse history.

## Vim map, noremap, remap

`remap` is an **option** that makes mappings work recursively. By default it is on and I'd recommend you leave it that way. The rest are **mapping commands**, described below:

`:map` and `noremap` are **recursive** and **non-recursive** versions of the various mapping commands. What that means is that if you do:

```bash
:map j gg
:map Q j
:noremap W j
```

`j` will be mapped to `gg`. `Q` will also be mapped to `gg`, because `j` will be expanded for the recursive mapping. `W` will be mapped to `j` (and not to `gg`) because `j` will not be expanded for the non-recursive mapping.

Now remember that Vim is a **modal editor**. It has a **normal** mode, **visual** mode and other modes.

For each of these sets of mappings, there is a mapping that works in normal, visual, select and operator modes (`:map` and `:noremap`), one that works in normal mode (`:nmap`and `nnoremap`), one in visual mode (`:vmap` and `:vnoremap`) and so on.

`map` is the "root" of all recursive mapping commands. The root form applies to "normal", "visual+select", and "operator-pending" modes.

`noremap` is the "root" of all non-recursive mapping commands. The root form applies to the same modes as map.

(Note that there are also the `!` modes like `map!` that apply to insert & command-line.)

**"Recursive"** means that the mapping is expanded to a result, then the result is expanded to another result, and so on.

The expansion stops when one of these is true:

the result is no longer mapped to anything else.
a non-recursive mapping has been applied (i.e. the "noremap" [or one of its ilk] is the final expansion).
At that point, vim's default "meaning" of the final result is applied/executed.

**"Non-recursive"** means the mapping is only expanded once, and that result is applied/executed.

Example:

```bash
nmap K H
nnoremap H G
nnoremap G gg
```
The above causes `K` to expand to `H`, then `H` to expand to `G` and stop. It stops because of the nnoremap, which expands and stops immediately. The meaning of `G` will be executed (i.e. "jump to last line"). At most one non-recursive mapping will ever be applied in an expansion chain (it would be the last expansion to happen).

The mapping of `G` to gg only applies if you press `G`, but not if you press `K`. This mapping doesn't affect pressing `K` regardless of whether `G` was mapped recursively or not, since it's line 2 that causes the expansion of K to stop, so line 3 wouldn't be used.

## ZSH
### 1Cycle through matches in ZSH

```bash
# Search backwards and forwards with a pattern
bindkey -M vicmd '/' history-incremental-pattern-search-backward
bindkey -M vicmd '?' history-incremental-pattern-search-forward

# set up for insert mode too
bindkey -M viins '^R' history-incremental-pattern-search-backward
bindkey -M viins '^F' history-incremental-pattern-search-forward
```

## Mac remap right command key to left ctrl

- to reset any key, you simply run the command again with that key's value in both Src and Dst

```
hidutil property --set '{"UserKeyMapping":
    [{"HIDKeyboardModifierMappingSrc":0x7000000e7,
      "HIDKeyboardModifierMappingDst":0x7000000e0}]
}'
```

0xe7 is the hex number for right command (right GUI)
0xe0 is the hex number for left CTRL (right GUI)

* Your changes will be lost at system reboot. If you want them to persist, put them in a script and setup a login hook:
```
chmod +x /Users/Shared/login_script.sh
sudo defaults write com.apple.loginwindow LoginHook /Users/Shared/login_script.sh
```

* Place your script, e.g., Test.sh, in a shared location - e.g., `/Users/Shared`

- and make sure it is executable (`chmod +x /Users/Shared/Test.sh`).

* From Terminal.app, run the following:
`sudo defaults write com.apple.loginwindow LoginHook /Users/Shared/Test.sh`

-------------------------------------------------------------

```
hidutil property --set '{"UserKeyMapping":
    [{"HIDKeyboardModifierMappingSrc":0x7000000e6,
      "HIDKeyboardModifierMappingDst":0x7000000e4}]
}'
```

Note that the above command is not switching the Right Alt (e6) and Right Control(e4). They will both be Right Control. If you have a MacBook, you will not notice this until plugging in an external keyboard. If you want to switch Right Alt and Right Control, you need to add a second switch command, like the following.

```
hidutil property --set '{"UserKeyMapping":
    [{"HIDKeyboardModifierMappingSrc":0x7000000e4,
      "HIDKeyboardModifierMappingDst":0x7000000e6},
     {"HIDKeyboardModifierMappingSrc":0x7000000e6,
      "HIDKeyboardModifierMappingDst":0x7000000e4}]
}’
```

To see the current mapping:

`hidutil property --get "UserKeyMapping"`

----------------------------------
The table at the bottom of the Technical Note has a list of hex values for each key. To generalize the above answer to switch any keys, you must or the hex value from that list together with `0x700000000`. The following Python code demonstrates one way to do this.

In [1]: def convert(val):
   ...:     int_val = int(val, 16)
   ...:     ref = '0x700000000'
   ...:     int_ref = int(ref, 16)
   ...:
   ...:     return hex(int_ref | int_val)
   ...:

In [2]: r_alt = '0xE6'

In [3]: print(convert(r_alt))
0x7000000e6


Ref:
https://apple.stackexchange.com/questions/283252/how-do-i-remap-a-key-in-macos-sierra-e-g-right-alt-to-right-control
https://developer.apple.com/library/archive/technotes/tn2450/_index.html#//apple_ref/doc/uid/DTS40017618-CH1-KEY_TABLE_USAGES
https://stackoverflow.com/questions/127591/using-caps-lock-as-esc-in-mac-os-x/46460200#46460200
	
## Proxy setting for iTerm2

https://blog.csdn.net/DSZhappy/article/details/108393159?spm=1001.2101.3001.6661.1&utm_medium=distribute.pc_relevant_t0.none-task-blog-2%7Edefault%7ECTRLIST%7Edefault-1.pc_relevant_aa&depth_1-utm_source=distribute.pc_relevant_t0.none-task-blog-2%7Edefault%7ECTRLIST%7Edefault-1.pc_relevant_aa&utm_relevant_index=1
	
test:
	curl -vv https://www.google.com
