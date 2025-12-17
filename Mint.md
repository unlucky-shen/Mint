# Linux Mint Documentation

## Enable ufw 


## Nvidia Proprietary via "Driver Manager"


## Remove Packages

1. Use Webapp Manager to delete "matrix"

```bash
sudo apt purge thunderbird celluloid hypnotix aisleriot gnome-mahjongg gnome-mines gnome-sudoku simple-scan drawing webapp-manager yelp firefox* rhythmbox warpinator xreader gnome-calculator gnome-calendar gucharmap sticky xed seahorse onboard fingwit mintinstall pix transmission-common transmission-gtk transmission -y
```


## Dev Tools
```bash
# Kitty Terminal
curl -L https://sw.kovidgoyal.net/kitty/installer.sh | sh /dev/stdin

# NVM (Nodejs-LTS)
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
nvm install --lts
npm install -g tree-sitter-cli
npm install -g prettier

# Rust (Rustup)
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

# uv-astral
curl -LsSf https://astral.sh/uv/install.sh | sh

# Starship Prompt
curl -sS https://starship.rs/install.sh | sh
```


## Add Repos

```bash
# Neovim Unstable
sudo add-apt-repository ppa:neovim-ppa/unstable
sudo apt update

# Multiverse - Enabled by default in Mint
```


## Install Essential Packages

```bash
sudo apt install wget curl xclip unzip p7zip-full libarchive-tools flatpak htop openssh-client openssh-server fzf ripgrep fd-find zathura tmux gcc gfortran python3 mesa-utils vulkan-tools libvulkan1 vulkan-validationlayers mesa-vulkan-drivers -y
```

## Flatpaks

```bash
flatpak install flathub io.gitlab.librewolf-community

flatpak install flathub com.brave.Browser

flatpak install flathub org.libreoffice.LibreOffice

flatpak install flathub com.discordapp.Discord

flatpak install flathub net.davidotek.pupgui2

flatpak install flathub com.spotify.Client

flatpak install flathub org.gimp.GIMP

flatpak install flathub org.kde.krita

flatpak install flathub org.kde.kdenlive
```


## R Language (Ubuntu 24.04)

### Pre-Requisites

```bash
sudo apt install --no-install-recommends software-properties-common dirmngr gnupg apt-transport-https ca-certificates -y
```

### Import CRAN GPG Key

```bash
wget -qO- https://cloud.r-project.org/bin/linux/ubuntu/marutter_pubkey.asc \
| sudo tee /etc/apt/trusted.gpg.d/cran_ubuntu_key.asc
```

### Add CRAN Repository

```bash
sudo tee /etc/apt/sources.list.d/cran.list <<EOF
deb https://cloud.r-project.org/bin/linux/ubuntu noble-cran40/
EOF
```

### Install R 

```bash
sudo apt install r-base r-base-dev
```

### R Packages 
```R
install.packages(c("tidyverse", "data.table", "janitor", "readxl", "openxlsx", "haven", "arrow", "lubridate", "fs", "here", "skimr", "ggthemes", "viridis", "patchwork", "modelr", "broom", "caret", "tidymodels", "rmarkdown", "knitr", "tinytex", "shiny", "roxygen2"))
```


## Typst

```bash
wget -qO typst.tar.xz https://github.com/typst/typst/releases/latest/download/typst-x86_64-unknown-linux-musl.tar.xz
```

```bash
sudo tar xf typst.tar.xz --strip-components=1 -C /usr/local/bin typst-x86_64-unknown-linux-musl/typst
```

```bash
rm -rf typst.tar.xz
```

#### To Uninstall
```bash
sudo rm -rf /usr/local/bin/typst
```
