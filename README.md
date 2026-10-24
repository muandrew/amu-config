# amu-config

A bunch of configs and settings that I'm just going to gather here.

```
cd $HOME
git clone git@github.com:muandrew/amu-config.git
source ${HOME}/amu-config/source.install
```
use source to pick up the existing shell, otherwise a default may be chosen

Tmux labels appear as `device · session · [session-name]` in the status bar,
and also prefix the terminal title:

```sh
trn laptop         # Device label, saved in ~/.config/amu_trn/env
tsrn project       # Current tmux session only; shared by its panes
trn ""             # Clear the device label
tsrn ""            # Clear the session label
```

`config/bashrc` loads the device label when the env file exists. Both commands
refresh attached tmux clients immediately. With both labels cleared, tmux uses
its default status and title text. After updating these configs, source
`config/bashrc` in your shell and run `tmux source-file ~/.config/tmux/tmux.conf`
in an existing tmux server.
