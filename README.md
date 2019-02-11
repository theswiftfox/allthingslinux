# Everything Linux, or whatever..
This repository will contain mostly guides and some scripts that I wrote and use on my linux machine (currently Manjaro).  
The main purpose of this repository is as a central place to store this stuff for myself, but feel free to use and edit everything.  
If you want to redistribute and give me some credit it is appreciated, but in no way required.  

# Adding commands for convenience to shell  
The file '.theswiftfoxrc' offers these commands:  
* ```open``` - opening the current folder in a file manager (change 'dde-file-manager' to the executable of the filemanager you are using)  
* ```cls``` - clear terminal screen while leaving scrollback intact  
* ```code``` - open specified file/folder in VSCode (I'm using insider builds so change the command to your VS code command or remove)  
* ```ncode``` - open specified file/folder in new VSCode window  
* ```cheatsh``` - curl cht.sh for informations about a command/tool/... usage: "cheatsh git" or "cheatsh git/submodule"  

To add these RCs to your shell, copy or ln -s '.theswiftfoxrc' to your home folder and add this line at the end of your .zshrc or .bashrc or .whateveryourrcis:  
```source ~/.theswiftfoxrc```  

# Table of Contents (I will try to keep this up to date)  

## Older Guides  
* [Setting up gnome3 on Ubuntu based distros](ubuntu_setup_gnome3.md)
* [Edit files from your remote server via local VSCode](vscode_rmate.md)
