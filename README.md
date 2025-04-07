# python-mac-venv

## Install Homebrew

The latest documentation is [here](https://brew.sh)
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## Install python

[Check](https://www.python.org/downloads/macos/) which version of python is the latest stable. It's currently 3.13

Install it:
```bash
brew install python@3.13
```

## Create venv

```bash
export VENV_DIR=/opt/tools
sudo mkdir $VENV_DIR
sudo chown $(whoami):$(id -g) $VENV_DIR

python3.13 -m venv $VENV_DIR
```

## Install packages

```bash
source $VENV_DIR/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```