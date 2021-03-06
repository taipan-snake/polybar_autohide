# PolyBar_Autohide
Polybar is a beautiful bar but in some cases for example if you have a small screen it might take too much space so I've made a simple script that hide Polybar when there are windows in the current workspace, the script shows the bar if you move the cursor where the bar is or if you don't have any windows in the workspace that you're using.

## How to Install
1. Clone the git repo in your home: 
     ```
     git clone https://github.com/arkeane/polybar_autohide.git ~/polybar_autohide
     ```
     - Install nedeed software: `polybar` `xdotool` `xdo`

2. Move to the script directory `cd ~/polybar_autohide`
     
3. Make adjustments to the script
     - You can adjust polybar_height definition to change sensibility.
     - You can also change paths but be carefull!!!

4. Compile the script `make`

5. Autostart the script
     - Add the `autohide` file to your autostart system
          - If you use i3wm add this to your config file, change $USER with your username:
               ```
               exec --no-startup-id /home/$USER/polybar_autohide/polybar-autohide
               ```
          - If not just use your usual autostart system.

## Changes from upstream
- Removed hotkey support to avoid file I/O, since I'm not using it anyway
- Added some delays for mouse movements and window presence
- Tried to minimize calls to external calls by keeping more state in the script, to keep the script lightweight

## Known Problems (working on, but upstream not by me)
- Dual monitor setup works but in a strange way 
- Trying to convert all the shell commands to c++ syntax to avoid external programs
- Multiple bars support

If you want to support me (upstream person) [PayPalMe](https://paypal.me/LudovicoPestarino)
