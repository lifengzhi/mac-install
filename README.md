# mac-install

## xcode

App Store 搜 xcode 安装, 安装后打开并授权操作

## shadowsocks

<http://160.16.231.71/ssx-2.6.3.dmg>

## 搜狗输入法

<https://pinyin.sogou.com/mac/?r=pinyin>

## chrome

<https://www.google.com/chrome/browser/desktop/index.html>

## iTerm2

<https://www.iterm2.com/downloads.html>

## homebrew

`cd ~ && mkdir homebrew && curl -L https://github.com/Homebrew/brew/tarball/master | tar xz --strip 1 -C homebrew`

将 `homebrew/bin` 添加到环境变量

修改为中科大源
```
# 替换brew.git:
cd "$(brew --repo)"
git remote set-url origin https://mirrors.ustc.edu.cn/brew.git

# 替换homebrew-core.git:
cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core"
git remote set-url origin https://mirrors.ustc.edu.cn/homebrew-core.git

brew update
```

homebrew 加速 <http://w3cboy.com/post/2017/03/homebrew-speed-up/>

## zsh

`brew install zsh`

oh-my-zsh `sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`

编辑配置 `~/.zshrc`, 修改主题为 ys

## tmux

`brew install tmux`

编辑配置文件 `vim ~/.tmux.conf`
```
set -g prefix C-a
unbind C-b
set -g mouse on

# List of plugins
set -g @plugin 'tmux-plugins/tpm'
set -g @plugin 'tmux-plugins/tmux-sensible'
set -g @plugin 'tmux-plugins/tmux-resurrect'
set -g @plugin 'tmux-plugins/tmux-yank'

# Initialize TMUX plugin manager (keep this line at the very bottom of tmux.conf)
run '~/.tmux/plugins/tpm/tpm'
```

使配置生效 `tmux source-file ~/.tmux.conf`

安装 tmp `git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm`

安装 yank `git clone https://github.com/tmux-plugins/tmux-yank ~/clone/path`

修改 iTerm2 设置
1. Go into iTerm2's preferences.
2. Go to the "General" tab.
3. Check "Applications in terminal may access clipboard"

进入 tmux, 输入快捷键 prefix + I, 安装插件

## Alfred

<http://xclient.info/s/alfred.html?_=baf317d2a9932afca9b32c327f8a34c9>

## vscode

<https://code.visualstudio.com/download>

## github desktop

<https://desktop.github.com/>

## dash

<http://xclient.info/s/dash.html?_=baf317d2a9932afca9b32c327f8a34c9>

## nvm

`brew install nvm`

## vim

```
syntax on
set showmatch
set nu
set tabstop=4
set noexpandtab
setlocal noswapfile
set bufhidden=hide
set history=100
set hlsearch
set nobackup
set ruler
set rulerformat=%20(%2*%<%f%=\ %m%r\ %3l\ %c\ %p%%%)
set selection=exclusive
set selectmode=mouse,key
set formatoptions=tcrqn
set autoindent
set showcmd
au BufReadPost * if line("'\"") > 0|if line("'\"") <= line("$")|exe("norm '\"")|else|exe "norm $"|endif|endif
colorscheme desert
syntax enable
set tags=tags;
set backspace=indent,eol,start
let g:winManagerWindowLayout='FileExplorer|TagList'
nmap wm :WMToggle<cr>
let Tlist_Show_One_File=1
let Tlist_Exit_OnlyWindow=1
let g:miniBufExplMapCTabSwitchBufs=1
let g:miniBufExplorerMoreThanOne=2
nnoremap <silent> <F3> :Grep<CR>
let Grep_Default_Options='-r --exclude-dir=.svn'
set cscopequickfix=s-,c-,d-,i-,t-,e-
set nocompatible              " be iMproved, required
filetype off                  " required
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()
Bundle 'gmarik/Vundle.vim'
Bundle 'a.vim'
Bundle 'taglist.vim'
Bundle 'winmanager'
Bundle 'minibufexpl.vim'
Bundle 'grep.vim'
Bundle 'wolfpython/cscope_map.vim'
call vundle#end()            " required
filetype plugin indent on    " required
```

安装插件工具 `git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim`

安装插件 `vim +PluginInstall +qall`

## Dr. Cleaner Pro 内存/垃圾清理

<http://xclient.info/s/dr-cleaner-pro.html?_=baf317d2a9932afca9b32c327f8a34c9>

## Charles 抓包

<http://xclient.info/s/charles.html?_=baf317d2a9932afca9b32c327f8a34c9>

