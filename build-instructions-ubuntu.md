# Building instructions in Ubuntu 23.10 for ester Chats:
(internet access is required to download libraries and necessary programs)

Prerequisites for building ester Chats:
valac (install it by typing sudo apt install valac)
gee-0.8 (install it by typing sudo apt install libgee-0.8-dev )
cmake (install it by typing sudo apt install cmake)
msfgmt (install it by typing sudo apt install gettext)
libadwaita-1 (install it by typing sudo apt install libadwaita-1-dev)
gnutls (install it by typing sudo apt install gnutls-dev)
sqlite3 (install it by typing sudo apt install sqlite3)
webrtc-audio-processing (install it by typing sudo apt install libwebrtc-audio-processing-dev)
libgcrypt (install it by typing sudo apt install libgcrypt-dev)
libsoup-3.0 (install it by typing sudo apt install libsoup-3.0-dev)
libcanberra (install it by typing sudo apt install libcanberra-dev)
gpgme (install it by typing sudo apt install libgpgme-dev)
nice (install by typing sudo apt install libnice-dev)
gnupg (install it by typing sudo apt install python3-gnupg)
gstreamer1.0 (install it by typing sudo apt install libgstreamer1.0-dev)
libqrencode (install it by typing sudo apt install libqrencode-dev)
libsrtp2 (install it by typing sudo apt install libsrtp2-dev)
libsignal-protocol-c (install it by typing sudo apt install libsignal-protocol-c-dev)
gstreamer-app-1.0, gstreamer-audio-1.0, gstreamer-rtp-1.0 and gstreamer-video-1.0 (install them by typing sudo apt install libgstreamer-plugins-base1.0-dev)

1. Download git (sudo apt install git)
2. Clone repo (git clone https://github.com/esterOSS/echats)
3. Go into echats directory
4. Type ./configure to check if all the necessary libraries are installed and to configure the build environment (if there are missing libraries then install them from the prerequisites list for building ester Chats)
5. To build it, type make
6. To install it, type sudo make install 
7. To fix the build, so that it loads the necessary compiled libraries and prevent the loading shared libraries error when launching it, type cd /etc/ld.so.conf.d/ , then create a local.conf file with any CLI text editor (like nano) and edit the file so that it contains "/usr/local/lib" (without quotes) in the file, then save it.
8. To fix the missing icons, type sudo cp -r /home/[username]/echats/main/data/icons/scalable /usr/share/icons/hicolor
9. To run your freshly compilied build of ester Chats, type echats in the terminal or open the ester Chats icon inside of your desktop enviroment, and done!
