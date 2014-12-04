:::Please be carried out in self- responsibility.:::

// Procedure: mac startup sound mute
1) Create a Shell script.
$ sudo vi /Library/Scripts/mute-on.sh

*the following script.
------------
#!/bin/bash
osascript -e 'set volume with output muted'
------------

2) Authority setting.
$ sudo chmod 744 /Library/Scripts/mute-on.sh 

3) LogoutHook check.
$ sudo defaults read com.apple.loginwindow LogoutHook

4) LogoutHook setting.
$ sudo defaults write com.apple.loginwindow LogoutHook /Library/Scripts/mute-on.sh 
 


// Return Procedure
1) 
$ sudo defaults delete com.apple.loginwindow LogoutHook

2)
$ sudo rm /Library/Scripts/mute-on.sh

EOF
