# mcService
A simple service I wrote to run minecraft java servers under a linux systemd service

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

# How to use

## Adding a server
Add your minecraft server(java) into a subfolder in the `~./minecraft` folder.
It should look like this:

```bash
user@server ~/minecraft$ tree -dL 1 ~/minecraft/
/home/user/minecraft/
|-- Create
|-- MechanicalMastery-1.3.0
|-- architect
|-- createTogether
|-- encrypted
|-- expert
`-- more

7 directories
```
each sub-dir of the minecraft contains a server for example MechanicalMastery-1.3.0:
```bash
user@server ~/minecraft/MechanicalMastery-1.3.0$ tree -L 1 .
|-- banned-ips.json
|-- banned-players.json
|-- config
|-- defaultconfigs
|-- eula.txt
|-- icon.png
|-- kubejs
|-- libraries
|-- local
|-- logs
|-- mods
|-- ops.json
|-- packmenu
|-- patchouli_books
|-- quests_structures
|-- rhino.local.properties
|-- run.sh
|-- server.properties
|-- skyblock_exports
|-- user_jvm_args.txt
|-- usercache.json
|-- usernamecache.json
|-- whitelist.json
`-- world

12 directories, 12 files
```

The important part is the `run.sh`. It is used to start the server, ensure it is marked as execute using `chmod +x ./run.sh`. Most server downloads or modpacks will provide this file.

## 