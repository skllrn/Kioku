# Tricks
## VBox Shared folder
mount -t vboxsf -o uid=$UID,gid=$(id -g) Shared ~/host
## diff checksum
diff <(md5sum some_file.txt) <(echo 7393checksum#937)
## Write image to medium
dd bs=4M if=2018-04-18-raspbian-stretch.img of=/dev/sdX conv=fsync status=progress
## list all setuid enabled files
find / -xdev \( -perm -4000 \) -type f -print0 | xargs -0 ls -l
## Download content of webpage
wget -p -r -E -e robots=off --convert-links -U mozilla --level 1 some.site
## Generate QR code for Wifi
qrencode -o wifi.png "WIFI:S:blauesBison;T:WPA2;P:dOiV4EQVTKC3kjzgPPEs;;"
## Run .img file with QEMU
qemu-system-i386 -drive format=raw,if=floppy,file=test.img -nographic
891-97-8933-91734-52
