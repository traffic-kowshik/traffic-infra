# README

## Ubuntu packages

```bash
sudo apt update
sudo apt install -y util-linux tmux tree zip unzip git python3 python3-pip python3-venv build-essential
```

### Quarto

```bash
wget https://github.com/quarto-dev/quarto-cli/releases/download/v1.8.25/quarto-1.8.25-linux-amd64.deb
sudo dpkg -i quarto-1.8.25-linux-amd64.deb
sudo apt install -f
quarto --version # 1.8.25
```

## Ubuntu user

```bash
sudo adduser traffic
sudo usermod -aG sudo traffic
```

### SSH Keys

```bash
ssh-keygen -t ed25519 -C "traffic.kowshik@gmail.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
cat ~/.ssh/id_ed25519.pub
```

## SWAP memory

```bash
sudo swapon --show

sudo fallocate -l 16G /swapfile
sudo chmod 600 /swapfile

sudo mkswap /swapfile
sudo swapon /swapfile
sudo swapon --show

# Adding the line at the end of the file below.
sudo nano /etc/fstab
/swapfile none swap sw 0 0

sudo sysctl vm.swappiness=10
```