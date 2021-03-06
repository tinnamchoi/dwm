dwm - dynamic window manager
============================
dwm is an extremely fast, small, and dynamic window manager for X.


Requirements
------------
In order to build dwm you need the Xlib header files.


Installation
------------
Edit config.mk to match your local setup (dwm is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install dwm (if
necessary as root):

    make clean install


Running dwm
-----------
Add the following line to your .xinitrc to start dwm using startx:

    exec dwm

In order to connect dwm to a specific display, make sure that
the DISPLAY environment variable is set correctly, e.g.:

    DISPLAY=foo.bar:1 exec dwm

(This will start dwm on display :1 of the host foo.bar.)

In order to display status info in the bar, you can do something
like this in your .xinitrc:

    while xsetroot -name "`date` `uptime | sed 's/.*,//'`"
    do
    	sleep 1
    done &
    exec dwm


Configuration
-------------
The configuration of dwm is done by creating a custom config.h
and (re)compiling the source code.

Custom hotkeys 
--------------
| Hotkey                        | Action                                                                           |
| ----------------------------- | -------------------------------------------------------------------------------- | 
| Alt+X                         | Spawn dmenu                                                                      |  
| Alt+Shift+X                   | Close window                                                                     |  
| Ctrl+Alt+X                    | Spawn st                                                                         |  
| Alt+Left/Right Arrow          | Change focus                                                                     |  
| Alt+Shift+Left/Right Arrow    | Change master size                                                               |  
| Alt+Up/Down Arrow             | Change number of windows in master                                               |  
| Alt+G                         | Gapless grid layout                                                              |  
| Alt+V                         | Centered master layout                                                           |  
| Alt+Space                     | Change layout                                                                    |
| Alt+E                         | PCManFM                                                                          |  
| Alt+R                         | OBS                                                                              |
| Alt+Shift+R                   | OBS with replay buffer on                                                        |
| Alt+A                         | pavucontrol                                                                      |
| Alt+S                         | [Spotify with adblock](https://github.com/tinnamchoi/bash-scripts)               |
| Alt+D                         | Discord                                                                          |  
| Alt+F                         | Firefox                                                                          |
| Alt+Shift+F                   | Chrome                                                                           |
| Alt+C                         | VS Code                                                                          |
| PrtSc                         | [Screenshot with maim and dmenu](https://github.com/tinnamchoi/bin#maim-dmenush) |
| Shift+PrtSc                   | [Quick screenshot with maim](https://github.com/tinnamchoi/bin#maim-dmenush)     |

List of official [patches](https://dwm.suckless.org/patches/) applied
---------------------------------------------------------------------
* [centeredmaster](https://dwm.suckless.org/patches/centeredmaster/)
* [dwmc](https://dwm.suckless.org/patches/dwmc/)
* [gaplessgrid](https://dwm.suckless.org/patches/gaplessgrid/)
* [hide vacant tags](https://dwm.suckless.org/patches/hide_vacant_tags/)
* [layoutscroll](https://dwm.suckless.org/patches/layoutscroll/)
* [swallow](https://dwm.suckless.org/patches/swallow/)
* [systray](https://dwm.suckless.org/patches/systray/)

> Note: The swallow patch is temporarily removed due to the current lack of option for toggling.
