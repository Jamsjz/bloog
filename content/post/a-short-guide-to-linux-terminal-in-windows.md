---
date: 2024-09-04
title: A short guide to linux terminal in windows
---

## Install WSL

1. Open control panel
2. Set the 'view by' to category
3. Go to 'programs and features'
4. Click on 'turn windows features on or off'
5. Click on 'Windows subsystem for linux', 'Virtual machine platform', and 'Hyper-V' or 'Hypervisor platform'
6. Restart your computer

## Install Ubuntu

1. Open the start menu
2. Search for powershell
3. Right click on powershell and select 'run as administrator'
4. Type `wsl --update` and the press enter and `wsl --install ubuntu-22.04` then press enter and `wsl --set-default-version 2` then press enter.
5. Wait for the installation to finish
6. After the installation is complete, it may ask you for a username and password.
7. After the installation is complete, open microsoft store and search for 'windows terminal'
8. Click on 'install'
9. Open the start menu and search for windows terminal
10. Open it. You should see a terminal window open with a drop down menu at the top. Click on the drop down menu and select 'ubuntu-22.04'
11. You should now be in the Ubuntu terminal

NOTE: In case you fuck up and you messed up you password,
you can reset it by going to powershell (as administrator) and typing `wsl -u root` and then `passwd <username>`.
Replace `<username>` with your username.

## Install necessary packages

### Update and upgrade existing packages

```bash
sudo apt update
sudo apt upgrade
```

### Install packages

```bash
snap install code
snap install lazygit-gm
sudo apt install git wget curl zsh
sudo apt install python3 python3-pip
```

### A short guide on linux terminal

1. Navigating directories
   To go to specific directory, type `cd <directory path>`.

   <directory path> is in the format of `/home/username/path/to/directory`
   or `path/to/directory`.

   `path/to/directory` is the relative path from the current directory you are in.

   To see the path of the current directory, type `pwd`.

   To got the home directory, type `cd`. This will take you to the home directory of the current user.

   To go to the root directory, type `cd /`.

   `/` is the root directory of the file system.

   `~` is the home directory of the current user.

2. Handling files
   To create a new file type touch `<file path>`.

   For example:

   ```bash
   touch hello.txt
   touch codes/hello.txt
   ```

   To create a directory, type `mkdir <directory path>`.

   For example:

   ```bash
   mkdir hello
   ```

   To copy a file, type `cp <source path> <destination path>`.

   To move a file, type `mv <source path> <destination path>`.

   To rename a file, type `mv <current.name> <new.name>`.

   To delete a file, type `rm <file path>`.

   To delete a directory, type `rm -r <directory path>`.
   If any problem occurs, type `rm -rf <directory path>`.

3. Searching files
   To search for a file, type `find <directory path> -name <file name>`.

   For example:

   ```bash
   find . -name hello.txt
   ```

   NOTE:
   `.` is the current directory.
   `..` is the parent or previous directory. For eg: if you are in `codes/hello/` folder the hello is the current directory and codes is the parent directory.

   That means `cd ..` will take you to the parent directory.
   And, `touch ../hello.txt` will create a file in the parent directory.
   And likewise for all other commands.

   This will search for the file hello.txt in the current directory.

4. Opening files
   To open a file, using default application, type `open <file path>`.

   To open a file using vscode type `code <file path>`.

---

## More Resources

1. [Linux Terminal Cheat Sheet](https://quickref.me/bash)
2. [python cheat sheet](https://quickref.me/python)
3. [git cheat sheet](https://quickref.me/git)
4. [wsl cheat sheet]()
5. [Managing virtual environments](https://medium.com/@adocquin/mastering-python-virtual-environments-with-pyenv-and-pyenv-virtualenv-c4e017c0b173)
