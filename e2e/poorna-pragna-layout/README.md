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
