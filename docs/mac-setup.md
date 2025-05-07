# Setting up a new mac for devs

1. Install Chrome browser: https://www.google.com/intl/en_au/chrome/

2. Install brew https://brew.sh/

Then use brew to install:

- [iterm2 (a better terminal)](https://formulae.brew.sh/cask/iterm2#default) → `brew install --cask iterm2`
- [zhs (add functions to the terminal)](https://formulae.brew.sh/formula/zsh#default) → `brew install zsh`
- [oh-my-zsh (framework for managing zsh configuration)](https://ohmyz.sh/) → `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
- [PowerLevel10k (for the terminal to look cooler)](https://github.com/romkatv/powerlevel10k)
- [fzf (to easily search all previous commands using crtl+r)](https://formulae.brew.sh/formula/fzf#default) → `brew install fzf`
- [nvm (version manager for node)](https://formulae.brew.sh/formula/nvm) → `brew install nvm` then add to .zshrc:
```bash
export NVM_DIR="$HOME/.nvm"
  [ -s "$HOMEBREW_PREFIX/opt/nvm/nvm.sh" ] && \. "$HOMEBREW_PREFIX/opt/nvm/nvm.sh" # This loads nvm
  [ -s "$HOMEBREW_PREFIX/opt/nvm/etc/bash_completion.d/nvm" ] && \. "$HOMEBREW_PREFIX/opt/nvm/etc/bash_completion.d/nvm" # This loads nvm bash_completion
```
- [git (version control)](https://formulae.brew.sh/formula/git#default) → `brew install git` then add username and email:
```bash
git config --global user.name "Rodrigo Ibanez"
git config --global user.email "rsibanez89@gmail.com"
```
- [Python 3.13](https://formulae.brew.sh/formula/python@3.13#default) → `brew install python@3.13`
- [awscli (aws command line interface)](https://formulae.brew.sh/formula/awscli#default) → `brew install awscli`
- [docker (container management)](https://formulae.brew.sh/formula/docker#default) → `brew install --cask docker`
- [Visual Studio Code Insiders (code editor)](https://formulae.brew.sh/cask/visual-studio-code@insiders#default) → `brew install --cask visual-studio-code@insiders`
- [jq (command-line JSON processor)](https://formulae.brew.sh/formula/jq#default) → `brew install jq`
- [just (command runner)](https://formulae.brew.sh/formula/just#default) → `brew install just`
- [z (change directory quickly)](https://formulae.brew.sh/formula/z#default) → `brew install z`

3. [Install Rectangle to manage windows like windows](https://rectangleapp.com/)

4. Change some default settings:
- Remove delay of dock appearing: `defaults write com.apple.Dock autohide-delay -float 0 && killall Dock`
- Show all hidden files `defaults write com.apple.finder AppleShowAllFiles TRUE && killall Finder`
- Speed up animation: `defaults write NSGlobalDomain NSWindowResizeTime -float 0.001 && killall Finder`
- Alert volumes to 0: `osascript -e "set volume alert volume 0"`
