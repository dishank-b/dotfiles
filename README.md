# Setting up terminal/shell workflow

- Terminal: iTerm2 (macOS)
- Shell: zsh (stable ecosystem)
- Change nano editor to link to nano instead of pico. 
- Prompt: Starship — single binary, cross-shell, fast and configurable.
- Multiplexer: tmux (session persistence, splits). Consider tmuxinator or tmuxp for project layouts.
- Fuzzy finder: fzf — indispensable for file / history / git branch pickers.
- Search & replacement: ripgrep (rg) + fd (fast file finder).
- Pretty file listing / pager: exa instead of ls, bat instead of cat.
- Git helpers: delta (diff pager), lazygit (TUI), gh (GitHub CLI).
- Language/tool version managers: asdf (multi), or volta for JS/Node, pyenv for Python.
- Environment guards: direnv (auto-load env per directory).
- Password manager: pass or gopass (CLI-friendly).
- Editor in terminal: neovim (fast, extensible).


## Shell setup
1. Iterm setup
    1. Import iterm profile to load settings config
    2. Enable natural text editing (ie to enable word/line level moving or deletion using option/ctrl) 
2. Set `zsh` as default shell via `chsh -s $(which zsh)`
3. Installing oh my zsh
    1. Install via: `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
    2. Write aliases and other env vars in size $ZSH_CUSTOM directory. 
    3. Get starship or powerlevel10k prompt.
        1. Configure the powerlevel10k -> get transient prompt
    4. Install zsh-autosuggestions and zsh-syntax-highlighting
4. install eza bat ripgrep btop delta tldr fzf
    1. Setup fzf config. setup `fzf` command - `export FZF_DEFAULT_COMMAND='rg --files --hidden --follow --glob "!.git"'`
