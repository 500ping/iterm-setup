# Introduce

My `iterm2` setup.

## Installation

- Install `Iterm2`

```bash
brew install --cask iterm2
```

- Set text color
```
iTerm → Preferences → Profiles → Colors → Color presets → Import → 
Color presets → file preset (Clovis-iTerm2-Color-Scheme.itermcolors)
```

- Change font
```
iTerm2 → Preferences → Profiles → Text → Change Font (Meslo LG M for Powerline)
```

- Install ZSH
```bash
brew install zsh zsh-completions
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

- Install Powerlevel9k Zsh
```bash
git clone https://github.com/bhilburn/powerlevel9k.git ~/.oh-my-zsh/custom/themes/powerlevel9k
```
Update ~/.zshrc
```bash
ZSH_THEME="powerlevel9k/powerlevel9k"
```

- ZSH Settings
```bash
# Add a space in the first prompt
POWERLEVEL9K_MULTILINE_FIRST_PROMPT_PREFIX="%f"
# Visual customisation of the second prompt line
local user_symbol="$"
if [[ $(print -P "%#") =~ "#" ]]; then
    user_symbol = "#"
fi
POWERLEVEL9K_MULTILINE_LAST_PROMPT_PREFIX="%{%B%F{black}%K{yellow}%} $user_symbol%{%b%f%k%F{yellow}%}  %{%f%}"
POWERLEVEL9K_LEFT_PROMPT_ELEMENTS=(dir rbenv vcs)
POWERLEVEL9K_RIGHT_PROMPT_ELEMENTS=(status root_indicator background_jobs history time)
POWERLEVEL9K_PROMPT_ON_NEWLINE=true
POWERLEVEL9K_PROMPT_ADD_NEWLINE=true
POWERLEVEL9K_VCS_MODIFIED_BACKGROUND='red'
```

- Autosuggestion
```bash
git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions

# Add to ~/.zshrc
plugins=(
    …
    zsh-autosuggestions
)
```

- Text Highlight
```bash
brew install zsh-syntax-highlighting
source $(brew --prefix)/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
```

- Additional settings
```
iTerm2 → Preferences → Profiles → Text
→ Cursor : ✓ Vertical Bar 
→ Blinking cursor : ✓ ON

iTerm → Preferences → Profiles → Keys → Load Preset… → Natural Text Editing
```

## Additional
- Fix Vscode font 
```json
{
    "terminal.integrated.fontFamily": "Meslo LG M for Powerline",
}
```