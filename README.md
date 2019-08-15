# iceberg-dark
Theme for various programs, designed with love for [iceberg.vim](https://github.com/cocopon/iceberg.vim) theme. 

Meant to replace iceberg.vim in places, where original theme is hard to read.
## Currently supported:
### [lightline.vim](https://github.com/itchyny/lightline.vim):

Original iceberg theme: ![old](screenshots/lightline_old.png)

iceberg-dark theme: ![new](screenshots/lightline_new.png)

Code snippet with both themes side to side: ![code snippet](screenshots/code_snippet.png)

**Installation** via [vim-plug](https://github.com/junegunn/vim-plug): put `Plug 'gkeep/iceberg-dark'` in your init.vim/.vimrc and run `:PlugInstall` to **install** the theme.

Then put `let g:lightline = { 'colorscheme': 'icebergDark' }` in your init.vim/.vimrc to **enable** the theme.

### [tmux](https://github.com/tmux/tmux):

Initially made with [tmuxline.vim](https://github.com/edkolev/tmuxline.vim), but modified along the way.

![tmux screenshot](screenshots/tmux.png)

Installation: 

1. Clone the repo: `git clone https://github.com/gkeep/iceberg-dark`

2. Copy `.tmux/iceberg.tmux.conf` to `~/.tmux`

3. Add `source-file ~/.tmux/iceberg.tmux.conf` to your `~/.tmux.conf`

### [bumblebee-status](https://github.com/tobi-wan-kenobi/bumblebee-status):

![bumblebee-status](screenshots/bumblebee.png)

Installation is not required, available at [bumblebee-status repository](https://github.com/tobi-wan-kenobi/bumblebee-status)
