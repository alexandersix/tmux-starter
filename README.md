[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)

![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/alexandersix/tmux-starter)

![GitHub Release](https://img.shields.io/github/v/release/alexandersix/tmux-starter)

# Tmux Starter

For the developers interested in turbocharging their terminal workflows without taking days or weeks of time to get started, I give you my Tmux starter.

Tmux starter is simple: it is a set of instructions and a basic, no-frills Tmux configuration file that will get you up and running with an ergonomic version of Tmux in no time at all!

## Installation

### Prerequisites

- [Tmux (>=3.5)](https://github.com/tmux/tmux)
- Linux, macOS (maybe WSL–I don't have a Windows device to confirm)

### Steps

1. Clone this repository to your local machine

```bash
git clone git@github.com:alexandersix/tmux-starter.git
```

2. (optional) Back up your exiting `~/.tmux.conf` file

```bash
mv ~/.tmux.conf ~/.tmux.conf.bak
```

3. Symlink or copy the `.tmux.conf` file to your home directory

```bash

# Symlinking keeps the file up to date with new versions
ln -s ./tmux-starter/.tmux.conf ~/

# Copying moves the file but does NOT automatically keep it up to date
mv ./tmux-starter/.tmux.conf ~/

```

4. Restart & run `tmux`, and enjoy the configuration!

## Features

### Sane Defaults

- Disallow automatic window renaming
- Start windows at index 1 instead of 0
- Increase tmux history limit
- Increase display time for tmux messages
- Set up "aggressive resizing" (a tmux session will always resize to match the smallest client currently connected to it)
- Allow mouse usage

#### Vim-specific changes

- Update color profile to work with Vim/Nvim background colors
- Remove Vim switching delay

### Additional Keybindings

- `Prefix r`: reload tmux configuration
- `Ctrl+{h,j,k,l}`: move panes
- `Ctrl+{H, J, K, L}`: resize current pane
- `Prefix \`: split vertically
- `Prefix -`: split horizontally
- Pane navigation with awareness of Vim splits (thank you to Chris Toomey for this one! - [vim-tmux-navigator](https://github.com/christoomey/vim-tmux-navigator))

#### Removed Bindings

- Arrow keys for pane navigation
- `Prefix %` and `Prefix "` for pane splitting

## License

[MIT](https://choosealicense.com/licenses/mit/)
