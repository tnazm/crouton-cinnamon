# crouton-cinnamon

This repository is NOT crouton or a modified version of crouton. It is simply some files which make using Cinnamon possible on crouton chroots.

##### How do I install Cinnamon?

First of all, you need to have downloaded crouton to your Downloads folder in Chrome OS and have made an Ubuntu 14.04 chroot. You can also do this in Debian 8 Jessie. If you haven't done any of these, you can download crouton by clicking [here](https://github.com/dnschneid/crouton/archive/master.zip). Extract the folder and make sure you put the crouton file in your Downloads folder. Then, you can make a chroot. Press CTRL+ALT+T and then type in:
````
shell
````
and press enter. Then type:
````
sudo sh ~/Downloads/crouton -r trusty -t core
````
Installing crouton with the "core" target will not install Xorg or a desktop environment. This is fine for us, since we're going to install Cinnamon from inside the chroot from the terminal and that will pull in Xorg. Once the installation is done, type in:
````
sudo enter-chroot
````
If you've used crouton before, you may wonder why you're not entering a new environment. This is because core only lets you use the command line. You're now operating from inside the chroot. You should first update and then upgrade everything in your chroot. Type in:
````
sudo apt-get update && sudo apt-get upgrade
````
Next, do:
````
sudo apt-get install cinnamon
````
This will install Cinnamon. However, you won't be able to use Cinnamon yet.

Click [here](https://github.com/Tenn1518/crouton-cinnamon/archive/master.zip) in order to download the files needed to boot Cinnamon from your chroot. Unzip master.zip and
