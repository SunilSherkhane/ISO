System requirements for building
A FreeBSD or helloSystem installed on the computer. The FreeBSD version needs to match the FreeBSD version of the helloSystem ISO being built (e.g., 12.2-RELEASE)

2 GHz dual core processor

4 GiB RAM (system memory)

50 GB of hard-drive space

Either a CD-RW/DVD-RW drive or a USB port for writing the Live media

A fast internet connection

Building the Live ISO
sudo pkg install -y pkg git-lite zsync wget sha bash zip devel/py-xdg librsvg2 ca_root_nss
git clone https://github.com/helloSystem/ISO
cd ISO
sudo ./build.sh hello
The resulting Live ISO will be located at /usr/local/furybsd/iso/.

Writing Live Media to USB drive
sudo dd if=/usr/local/furybsd/iso/FuryBSD-12.1-XFCE.iso of=/dev/daX bs=4m status=progress
Replace daX with the respective device name.

