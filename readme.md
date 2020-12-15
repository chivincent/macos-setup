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
	wget curl vim zsh git \
	coreutils findutils gnu-tar gnu-sed gawk gnutls gnu-getopt grep \
	fzf htop gh git-flow-avh p7zip lsd jq \
	composer nodejs go rust python
```

#### Cask

```
brew install --cask \
	microsoft-edge dropbox squirrel protonvpn protonmail-bridge \
	iterm2 visual-studio-code docker lens phpstorm
```

#### Fonts

```
brew install --cask \
	font-source-code-pro \
	font-noto-sans font-noto-sans-cjk-tc font-noto-serif font-noto-serif-cjk-tc \
	font-jetbrains-mono
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

### PHP

```
composer global require phpunit/phpunit psy/psysh
```

### Python

```
pip install fastapi unvicorn
```

### Nodejs

```
npm install -g typescript
```

### GH

```
gh auth login --web
gh config set git_protocol ssh
```


