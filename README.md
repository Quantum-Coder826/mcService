# mcService
A simple service I wrote to run minecraft servers under a linux systemd service

# installation

## preparations
check if you have `screen` installed, if it isn't pleas install the screen package by running:
```bash
sudo apt install screen
```

## automatic installation script
For automatic installation copy the following line and run it in the terminal.
```bash
wget -O - https://raw.githubusercontent.com/Quantum-Coder826/mcService/master/installer.sh | tr -d '\r' | bash
```
>**note**
> The install script is kinda dumb so it might fail.

## manual installation
- Create the following folder if it does not exist: `~/.config/systemd/user/`
- Copy/download the `mc@.service` file to that folder.
- Create a `minecraft` folder in your home directory.

