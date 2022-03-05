# Terminal Setup

## Xfce-Terminal
```
sudo apt-get install xfce4-terminal

# Update Shortcuts to terminal
sudo update-alternatives --config x-terminal-emulator

# Link config file
mkdir -p ~/.config/xfce4/terminal/
ln -s `pwd`/configs/xfce ~/.config/xfce4/terminal/terminalrc
```

## Zsh
```
sudo apt install zsh

# set to default shell
chsh -s $(which zsh)

# load configuration
ln -s `pwd`/configs/zshrc ~/.zshrc
```

### Oh my zsh
```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### Powerlevel10k
Install Fonts
- [MesloLGS NF Regular.ttf](
    https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Regular.ttf)
- [MesloLGS NF Bold.ttf](
    https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold.ttf)
- [MesloLGS NF Italic.ttf](
    https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Italic.ttf)
- [MesloLGS NF Bold Italic.ttf](
    https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold%20Italic.ttf)

Install theme
```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k

# load configuration
ln -s `pwd`/configs/p10k ~/.p10k.zsh
```

### Syntax Highlighting
```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

### Auto-suggestions
```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

## Git

```
sudo apt install git
```

```
git config --global user.name "t1mkhuan9"
git config --global user.email "timkhuang@icloud.com"
git config --global credential.helper store
```
