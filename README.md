# TGM-Linux-Printing
I wrote this guide for myself because I know that I will someday reset my
operating system and have no idea how to set it up again.

_You need CUPS._

Install **samba**:
```zsh
sudo pacman -S samba
```

Create the File `/etc/samba/smb.conf`:
```zsh
sudo touch /etc/samba/smb.conf
```

_restart_

Open the CUPS Web-Interface: [http://localhost:631/admin](http://localhost:631/admin)
 - add a new printer
 - choose **Windows Printer via SAMBA**
 - enter `smb://`*USERNAME*`:`_PASSWORD_`@TGM/printsrv-01.tgm.ac.at/followyou` as url
 - name as you like
 - choose a PPD-File that supports PCL (for example [pxlcolor](https://www.openprinting.org/printer/Generic/Generic-PCL_6_PCL_XL_Printer))
 
## Problems
### Firefox PDF Reader
I cant use the internal print dialog from firefox, but it works if I click on *use system dialog*.

### It doesnt work
Just try to restart the printer in Gnome Settings 

## Helpful Links
 * "Drucker Installation unter MacOS"; TGM HIT How-To's [online](https://portal.tgm.ac.at/Anleitungen/TGM-Drucker-Installation-unter-MacOS.pdf)
 * "SAMBA client printer cannot add to cups"; archlinux Forum [online](https://bbs.archlinux.org/viewtopic.php?id=173334)
