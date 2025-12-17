# tmux config

My personal tmux configuration with Catppuccin theme and vim-style navigation.

## Features

- **Prefix**: `Ctrl+s`
- **Mouse support** enabled
- **Vim-style pane navigation** via vim-tmux-navigator (`Ctrl+h/j/k/l`)
- **Pane resizing** with `prefix + h/j/k/l`
- **Catppuccin theme** with top status bar
- **TPM** for plugin management

## Keybindings

| Key | Action |
|-----|--------|
| `Ctrl+s` | Prefix |
| `Ctrl+h/j/k/l` | Navigate panes (works inside nvim too) |
| `prefix + h/j/k/l` | Resize panes |
| `prefix + %` | Vertical split |
| `prefix + "` | Horizontal split |
| `prefix + x` | Kill pane |
| `prefix + z` | Toggle pane zoom |
| `prefix + d` | Detach session |
| `prefix + r` | Reload config |

## Installation
```bash
# Install tmux
brew install tmux

# Clone this repo and symlink config
git clone https://github.com/r0llingclouds/tmux.git ~/tmux
ln -sf ~/tmux/.tmux.conf ~/.tmux.conf

# Install TPM
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm

# Start tmux and install plugins
tmux
# Press Ctrl+s then Shift+I to install plugins
```

## Plugins

- [tpm](https://github.com/tmux-plugins/tpm) - Plugin manager
- [catppuccin/tmux](https://github.com/catppuccin/tmux) - Theme
- [vim-tmux-navigator](https://github.com/christoomey/vim-tmux-navigator) - Seamless navigation between vim and tmux panes

## Backup
```bash
# Add to ~/.zprofile
alias tmux-backup='cd ~/tmux && cp ~/.tmux.conf . && git add -A && git commit -m "backup tmux config" && git push && cd -'
alias tmux-restore='git clone https://github.com/r0llingclouds/tmux.git ~/tmux && ln -sf ~/tmux/.tmux.conf ~/.tmux.conf'
```
