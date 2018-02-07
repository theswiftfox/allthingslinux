# Using Visual Studio Code as editor via ssh

There is a great tool available called [rmate]() that can be used to edit files with your local editor when accessing a remote machine via ssh.  

# Setup

## Client side
#### VSCode
Within VSCode install [this](https://github.com/rafaelmaiolla/remote-vscode) extension.  
You can find it by searching for "Remote VSCode" in the extensions browser.  
Before you can edit files from remote via VSCode you just have to start the rmate server.  
You can do this in VSCode by pressing "F1" and typing "remote:startserver".  
Just remember you have to do this once after VSCode started to be able to edit files from your remote location.

#### SSH
When connecting via ssh you just have to make sure to use the remote-socket for rmate.  
Remote sockets are passed to ssh with the option "-R PORT:HOST:PORT"  
RMate uses port 52698 per default, so the ssh call would look like this:  
```
ssh -R 52698:localhost:52698 user@server
```

I usually am quite lazy with typing stuff, so I added an alias to my .zshrc:   
```
alias rssh="ssh -R 52698:localhost:52698"
```
Now I can just type "rssh user@server" and thats it.

## Server side
There are different implementations for rmate available and you should be able to use any of them you like. I did use the ruby version from [here](https://github.com/textmate/rmate)  

You can install rmate on your server with these commands:  
```
curl -Lo ~/bin/rmate https://raw.githubusercontent.com/textmate/rmate/master/bin/rmate
chmod a+x ~/bin/rmate
```
You can now edit files via "rmate FILE" and it will open on your local VSCode. It does also work with sudo.

If you want to keep the syntax for opening files with VSCode via remote as close to your local syntax you can rename or alias "rmate" to "rcode".  
