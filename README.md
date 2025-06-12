# .dotfiles
foolmalhar's dotfiles

Steps to bootstrap new Mac:

1. Install Apple's CLTools, which are prerequisites for Git and Homebrew.
```bash
xcode-select --install
```

2. Clone this repo into new hidden dir.
```bash
# use ssh if set up
git clone git@github.com:MaxxCode8/.dotfiles.git ~/.dotfiles

# or use HTTPS and switch users later.
git clone https://github.com/MaxxCode8/.dotfiles.git ~/.dotfiles
```

3. Create symlinks in home dir to the real files in the repo.
```bash
# install script required here ... or stow
ln -s ~/.dotfiles/.zshrc ~/.zshrc
ln -s ~/.dotfiles/.gitconfig ~/.gitconfig
```

4. Install homebrew, followed by the software listed in Brewfile.
```bash
# this can also be a stow or install script 

# Install homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Pass in the Brewfile location.
brew bundle --file ~/.dotfiles/Brewfile

# .. move to the dir first.
cd ~/.dotfiles && brew bundle 
```

## TODO: 
Include ALL configs
