# Code instructions: https://www.fosslinux.com/2808/how-to-clean-virus-by-command-line-scan-in-ubuntu-linux-mint.htm

## This is the command to install the program on debian/ubuntu based systems
sudo apt-get install clamav

## The freshclam database needs to be updated first.
sudo /etc/init.d/clamav-freshclam stop
sudo freshclam
sudo /etc/init.d/clamav-freshclam start

## This runs the antivirus program
clamscan -i -r ~/

## This removes any detected viruses
clamscan --remove=yes -i -r ~/
