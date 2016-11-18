# .tmux config
@rjhilgefort's tmux configuration. Best used as a submodule in your dotfiles.

# Features
- Modularized, broken out config with seperate files for seperate concerns
- TPM usage, included as a submodule
- OS specific configuration and condition sourcing of said config

# Usage
- TODO
  - Detail settings
  - Detail commands
    - Make table

- All prefixed with Ctrl-f
  - Last used window: /
  - Last used pane:   ;
  - Vertical split:   v
  - Horizontal split: s
  - Previous window:  [
  - Next window:      ]
  - Choose session:   Ctrl-s
  - Quick window:     Ctrl-q

# Installation

This setup depends on you cloning this repo to your home directory, and symlinking your normal `tmux.conf` to the `tmux.conf` within this project. There are, of course other ways of settings things up (for instance, I don't have it setup exactly this way on my machine). You could simply `source-file {path-to-this repo}/.tmux.conf`, but you would also have to change the paths there within. For simplicity, below is the advised way of setting things up.

```shell
cd ~
git clone git@github.com:rjhilgefort/.tmux.git .tmux
mv .tmux.conf .tmux.conf-SAVE # backup your potentially existing tmux config
ln -s .tmux/.tmux.conf .tmux.conf
tmux source ~/.tmux.conf
```

# TODO
- Check out sensible
- Rename files, no need for tmux prefix
- Conditionally include a gitignored user config file
- Consider just making this a TPM plugin. Current advantage is drop and go setup for brand new tmux users. Multi-install setup that caters to both types of users?
