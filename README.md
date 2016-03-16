# crouton-cinnamon

This repository is NOT crouton or a modified version of crouton. It is simply some files which make using Cinnamon possible on crouton chroots.

##### How do I use these files?
First, create a Linux chroot using crouton. You can create one with only the targets "core" and optionally "cli-extra". Open a Crosh window with CTRL+ALT+T. An example:
```
sudo sh ~/Downloads/crouton -r trusty -t core
```
will create a Linux chroot with Ubuntu 14.04. Then, you can enter the chroot with:
```
sudo enter-chroot
```
Now, you can install Cinnamon. First, add the Cinnamon PPA (since the trusty repos do not contain Cinnamon) and then install Cinnamon (you do not need to do this on Ubuntu 14.10+ and Debian 8+).
```
sudo apt-get install software-properties-common
sudo add-apt-repository ppa:lestscape/cinnamon
sudo apt-get update
sudo apt-get install cinnamon
```
We'll clone this repository to your Downloads folder so you can access it from Chrome OS and Linux, since crouton links the Downloads folder from each OS. Type in:
```
cd ~/Downloads
sudo apt-get install git
git clone https://github.com/Tenn1518/crouton-cinnamon
```
Next, type in:
```
cd crouton-cinnamon
cp Linux/xinitrc ~/.xinitrc
```
Now you can exit from the chroot by typing in:
```
exit
```
Now that you are back in Chrome OS, you should copy the startcinnamon script to your /usr/local/bin. Type in:
```
cd ~/Downloads/crouton-cinnamon
sudo cp Chrome\ OS/startcinnamon /usr/local/bin/startcinnamon
```
The chroot now has cinnamon installed, but it doesn't have xinit, which you need to start Cinnamon. You can install xinit by exiting the chroot with the "exit" command. Now, you can update your chroot and add the xorg target by:
```
sudo sh ~/Downloads/crouton -u -n trusty -t xorg
``` 
You may need to replace trusty if you installed a different release of trusty.
(Tutorial not finished)
