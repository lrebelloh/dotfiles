# About

Repository with all my dotfiles.

# Install

Firstly, install zsh:

```
  # OSX
  brew install zsh
  
  # Ubuntu
  apt install zsh -y
```

And then [oh my zsh](https://github.com/robbyrussell/oh-my-zsh):

```
  sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

The installation script should set zsh to default shell, but if it doesn't it can be do it manually:

```
  chsh -s $(which zsh)
```

Clone this repo:

```
  git clone git@github.com:lrebellos/dotfiles.git ~/.dotfiles
```

Grant permission to installation script and then run it:

```
chmod +x ~/.dotfiles/dotfiles.sh

~/.dotfiles/dotfiles.sh
```

#### Spaceship Theme:

Clone Spaceship repo:

```
  git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt"
```

Symlink `spaceship.zsh-theme` to your oh-my-zsh custom themes directory:

```
  ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"
```

#### Plugins:

```
  git clone git://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

  git clone https://github.com/zsh-users/zsh-autosuggestions       ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

  git clone https://github.com/zsh-users/zsh-completions           ${ZSH_CUSTOM:=~/.oh-my-zsh/custom}/plugins/zsh-completions
```

#### Fira Code font

##### OSX

```
  brew tap homebrew/cask-fonts
  brew cask install font-fira-code
```

##### Ubuntu

```
sudo add-apt-repository universe
sudo apt install fonts-firacode
