# macOS Setup

## Homebrew

### Installation

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

> Note: Use `brew doctor` to check if install successfully.

### Softwares

#### Core Utils

```
brew install \
	wget curl vim zsh git svn \
	coreutils findutils gnu-tar gnu-sed gawk gnutls gnu-getopt grep \
	fzf htop gh git-flow-avh p7zip lsd jq \
	composer nodejs go rust python
```

#### Cask

```
brew install --cask squirrel
```

#### Fonts

```
brew tap homebrew/cask-fonts
brew install --cask \
	font-source-code-pro \
	font-noto-sans font-noto-sans-cjk-tc font-noto-serif font-noto-serif-cjk-tc \
	font-jetbrains-mono font-hack-nerd-font
```

## ZSH

### Auto Suggestion

```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

### .zshrc

```
cp dotfiles/zshrc ~/.zshrc
```

## Others

### PHP, Python and Nodejs

```
composer global require phpunit/phpunit psy/psysh
pip install fastapi unvicorn
npm install -g typescript
```

### GH

```
gh auth login --web
gh config set git_protocol ssh
```

### SSH

```
ssh-keygen -t ed25519 -C "mbp2016"
# ssh-keygen -t rsa -b 4096 -C "mbp2016"

cp conf/ssh_config ~/.ssh/config

eval "$(ssh-agent -s)"
ssh-add -K ~/.ssh/id_ed25519
# ssh-add -K ~/.ssh/id_rsa
```
