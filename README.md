# Mac OS X Tools Cheatsheet
New machine cheatsheet

## Homebrew & cask
```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew cask
brew tap buo/cask-upgrade
brew tap homebrew/cask-versions
```
## Mac App Store
```bash
brew install mas
```
## Terminal & Shell & iTerm2
```bash
# Terminal App
brew cask install iterm2
```
Get the iTerm color settings (patched version to fix the bright black value) and Font

* [Solarized Dark theme](https://raw.githubusercontent.com/mbadolato/iTerm2-Color-Schemes/master/schemes/Solarized%20Dark%20-%20Patched.itermcolors) (Save Link as...)
* [Meslo LG M DZ Regular for Powerline.ttf](https://raw.githubusercontent.com/powerline/fonts/master/Meslo%20Dotted/Meslo%20LG%20M%20DZ%20Regular%20for%20Powerline.ttf) (Save Link as...)

iTerm2 + Oh My Zsh + Solarized color scheme + Meslo powerline font->
[https://gist.github.com/kevin-smets/8568070](https://gist.github.com/kevin-smets/8568070)

```bash
# zsh
brew install zsh

# oh-my-zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

#plugins
brew install zsh-syntax-highlighting
brew install zsh-autosuggestions
echo "source /usr/local/share/zsh-autosuggestions/zsh-autosuggestions.zsh" >> ~/.zshrc
echo "source /usr/local/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> ~/.zshrc

# Don't show the user in the prompt
echo "DEFAULT_USER=\`whoami\`" >> ~/.zshrc

# Remove the 'last login' message
touch ~/.hushlogin

```
### Tweaking OSX Settings
```bash
# Finder: show hidden files by default
defaults write com.apple.finder AppleShowAllFiles -bool true

# Finder: show all filename extensions
defaults write NSGlobalDomain AppleShowAllExtensions -bool true

# Finder: allow text selection in Quick Look
defaults write com.apple.finder QLEnableTextSelection -bool true

# Disable auto-correct
defaults write NSGlobalDomain NSAutomaticSpellingCorrectionEnabled -bool false

# Require password immediately after sleep or screen saver begins
defaults write com.apple.screensaver askForPassword -int 1
defaults write com.apple.screensaver askForPasswordDelay -int 0

# Show the ~/Library folder
chflags nohidden ~/Library

# Don’t automatically rearrange Spaces based on most recent use
defaults write com.apple.dock mru-spaces -bool false

# Prevent Time Machine from prompting to use new hard drives as backup volume
defaults write com.apple.TimeMachine DoNotOfferNewDisksForBackup -bool true
```

### Common apps
```bash
# Default browser. I like Chrome.
brew cask install google-chrome

# Authy
brew cask install authy

# Spotify
brew cask install spotify

# The Unarchiver
brew cask install the-unarchiver

# VLC
brew cask install vlc

# coconutbattery
brew cask install coconutbattery
```

### Productivity
```bash
# Telegram
brew cask install telegram

# Slack
brew cask install slack

# Skitch
brew cask install skitch

# Spectacle
brew cask install spectacle

# Itsycal
brew cask install itsycal

# RecordIt
brew cask install recordit

# Amphetamine
mas install 937984704
```

### Development
```bash
# Text editors/IDEs
brew cask install sublime-text
brew cask install visual-studio-code

# Virtual
brew install --cask virtualbox
brew install --cask virtualbox-extension-pack

# API development
brew cask install postman
brew cask install paw

# Charles
brew cask install charles

# Docker
brew cask install docker
brew cask install kitematic

# Gas Mask
brew cask install gas-mask

# Ngrok
brew cask install ngrok

# Cloud storage and related
brew cask install cyberduck

# Databases
brew cask install sequel-pro

# VPS
brew cask install tunnelblick

# JQ
brew install jq

# Bat - https://github.com/sharkdp/bat
brew install bat

# Tree
brew install tree

# thefuck
brew install thefuck

# AWS CLI
brew install awscli
```

### Postgres
```bash
brew install postgres
brew services start postgresql
```

### Python
```bash
brew install python
brew install python3
brew install anaconda
```

### Java
```bash
# JetBrains
brew cask install intellij-idea

# Java
brew cask install java8

# Tomcat
brew install tomcat
```

### Swift & Objective-c
```bash
# Xcode
mas install 497799835
# Cocoapods
brew install cocoapods
```

## Google Chrome stuff
- https://chrome.google.com/webstore/detail/json-formatter/bcjindcccaagfpapjjmafapmmgkkhgoa
- https://chrome.google.com/webstore/detail/quick-qr-code-generator/afpbjjgbdimpioenaedcjgkaigggcdpp
- https://chrome.google.com/webstore/detail/adblock-plus-free-ad-bloc/cfhdojbkjhnklbpkdaibdccddilifddb
- https://chrome.google.com/webstore/detail/editthiscookie/fngmhnnpilhplaeedifhccceomclgfbg
