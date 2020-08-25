# iceberg-dark
Theme for various programs, designed with love for [iceberg.vim](https://github.com/cocopon/iceberg.vim) theme.

Meant to bring [iceberg.vim](https://github.com/cocopon/iceberg.vim) to other environments and to replace it in places, where original theme is hard to read.

<div align="center"><em>Lightline theme with tmux theme</em></div>

![lightline & slanted tmux screenshot](screenshots/lightline_tmux.png)

<div align="center"><em>Airline theme with minimal tmux theme</em></div>

![airline & tmux minimal screenshot](screenshots/airline_tmux.png)


**Requirements**:

* A [Nerd Font](https://github.com/ryanoasis/nerd-fonts/#patched-fonts) (if you don't use one already) for special characters support.

## Currently supported:

### [lightline.vim](https://github.com/itchyny/lightline.vim):

Original iceberg theme: ![old](screenshots/lightline_old.png)

iceberg-dark theme: ![new](screenshots/lightline_new.png)

Code snippet with both themes side to side: ![code snippet](screenshots/code_snippet.png)

**Installation** via [vim-plug](https://github.com/junegunn/vim-plug):

 1. Put `Plug 'gkeep/iceberg-dark'` in your init.vim/.vimrc

 2. Run `:PlugInstall` to **install** the theme.

 3. Put `let g:lightline = { 'colorscheme': 'icebergDark' }` in your init.vim/.vimrc to **enable** the theme.

### [vim-airline](https://github.com/vim-airline/vim-airline):

![airline](screenshots/airline.png)

**Installation** via [vim-plug](https://github.com/junegunn/vim-plug):

 1. Put `Plug 'gkeep/iceberg-dark'` in your init.vim/.vimrc

 2. Run `:PlugInstall` to **install** the theme.

 3. Put `let g:airline_theme='icebergDark'` in your init.vim/.vimrc to **enable** the theme.

### [tmux](https://github.com/tmux/tmux):

#### Minimal

Inspired by [this](https://www.reddit.com/r/unixporn/comments/e6x7lz/dwm_blue_stripes/) post at [r/unixporn](https://www.reddit.com/r/unixporn).

![tmux minimal screenshot](screenshots/tmux_minimal.png)

Installation:

1. Create `.tmux` folder in your home directory: `mkdir ~/.tmux`

2. To download, run the following command:
```
wget -O $HOME/.tmux/iceberg_minimal.tmux.conf \
https://raw.githubusercontent.com/gkeep/iceberg-dark/master/.tmux/iceberg_minimal.tmux.conf
```

3. Add `source-file ~/.tmux/iceberg_minimal.tmux.conf` to your `~/.tmux.conf`

#### With powerline symbols

#### 👀 NEW: Now with configurable modules and separators!

Configuration:

1. To configure modules edit `module_left_{1,2}` and `module_right_{1,2}`

By default, comes with **slants** style.

2. To configure separators edit `(sub)separator_left` and `(sub)separator_right`

By default displays `username` and `time` on the left and `local IP address` and `hostname` on the right.

##### Styles:

1. **Slants**:

![slanted tmux theme](screenshots/tmux_slanted.png)

```
# separators
separator_left="\ue0bc"
separator_right="\ue0ba"

subseparator_left="\ue0bb"
subseparator_right="\ue0bd"
```

2. **Rounded**:

![rounded tmux theme](screenshots/tmux_rounded.png)

```
# separators
separator_left="\ue0b4"
separator_right="\ue0b6"

subseparator_left="\ue0b5"
subseparator_right="\ue0b7"
```

3. **Powerline**:

![powerline tmux theme](screenshots/tmux_powerline.png)

```
# separators
separator_left="\ue0b0"
separator_right="\ue0b2"

subseparator_left="\ue0b1"
subseparator_right="\ue0b3"
```
Installation:

1. Create `.tmux` folder in your home directory: `mkdir ~/.tmux`

2. To download, run the following command:
```
wget -O $HOME/.tmux/iceberg.tmux.conf \
https://raw.githubusercontent.com/gkeep/iceberg-dark/master/.tmux/iceberg.tmux.conf
```

3. Add `source-file ~/.tmux/iceberg.tmux.conf` to your `~/.tmux.conf`

Example **iceberg.tmux.conf** configuration:
```tmux
# modules
module_left_1="#(whoami)"
module_left_2="%R %a"

module_right_1="#(ip route get 1 | awk '{print $7}')"
module_right_2="#H"

# separators
separator_left="\ue0bc"
separator_right="\ue0ba"

subseparator_left="\ue0bb"
subseparator_right="\ue0bd"
```

Example **tmux.conf**:
```tmux
source-file "$HOME/.tmux/iceberg.tmux.conf"

bind -r H resize-pane -L 5
bind -r J resize-pane -D 5
bind -r K resize-pane -U 5
bind -r L resize-pane -R 5

bind -n S-Left  previous-window
bind -n S-Right next-window
```

**_NOTE_**:
If you plan to use both minimal and powerline themes, you must comment out the unneeded one like this:

```tmux
#source-file "$HOME/.tmux/iceberg.tmux.conf"
source-file "$HOME/.tmux/iceberg_minimal.tmux.conf"
```
to use the minimal theme

or

```tmux
source-file "$HOME/.tmux/iceberg.tmux.conf"
#source-file "$HOME/.tmux/iceberg_minimal.tmux.conf"
```
to use the theme with powerline symbols.

### [bumblebee-status](https://github.com/tobi-wan-kenobi/bumblebee-status):

![bumblebee-status](screenshots/bumblebee.png)

Installation is not required, available at [bumblebee-status repository](https://github.com/tobi-wan-kenobi/bumblebee-status).

Source code available at the root of this repository.

## License

MIT license. See [LICENSE](https://github.com/gkeep/iceberg-dark/blob/master/LICENSE) for more information.
