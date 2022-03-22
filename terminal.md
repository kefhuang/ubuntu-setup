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
git config --global core.editor "vim"
```

## CUDA
Install the lastest the driver from Software and Updates
```
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2004/x86_64/cuda-ubuntu2004.pin
sudo mv cuda-ubuntu2004.pin /etc/apt/preferences.d/cuda-repository-pin-600
wget https://developer.download.nvidia.com/compute/cuda/11.6.1/local_installers/cuda-repo-ubuntu2004-11-6-local_11.6.1-510.47.03-1_amd64.deb
sudo dpkg -i cuda-repo-ubuntu2004-11-6-local_11.6.1-510.47.03-1_amd64.deb
sudo apt-key add /var/cuda-repo-ubuntu2004-11-6-local/7fa2af80.pub
sudo apt-get update
sudo apt-get -y install cuda
sudo apt-get -y install cuda-toolkit-11-6
```
Add `export PATH="/usr/local/cuda-11.6/bin:$PATH"` and
`export LD_LIBRARY_PATH="/usr/local/cuda-11.6/lib64:$LD_LIBRARY_PATH"` to `.bashrc` or `.zshrc`
if `nvcc` is not found.

## SSH
```
sudo apt install openssh-server
sudo systemctl restart ssh
sudo systemctl enable ssh
```

## Conda
```
sudo apt-get install libgl1-mesa-glx libegl1-mesa libxrandr2 libxrandr2 libxss1 libxcursor1 libxcomposite1 libasound2 libxi6 libxtst6
```
Download https://www.anaconda.com/products/individual/download-success-2
```
bash ~/Downloads/Anaconda3-2020.02-Linux-x86_64.sh
```
Choose no when ask to init
```
eval "$(/home/t1mkhuan9/Softwares/anaconda/bin/conda shell.zsh hook)"
conda init zsh
conda config --set auto_activate_base false
```

## Latex
```
sudo apt install texlive-full
```
