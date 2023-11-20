# Building instructions in Arch for ester Chats:
(internet access is required to download libraries and necessary programs)

Prerequisites for building ester Chats:
valac (install it by typing sudo pacman -S extra/valac)
ninja (install it by typing sudo pacman -S ninja)
cmake (install it by typing sudo pacman -S cmake)
libgcrypt (install it by typing sudo pacman -S libgcrypt)
libqrencode (install it by typing sudo pacman -S qrencode)
libsrtp2 (install it by typing sudo pacman -S extra/libsrtp2)
libsignal-protocol-c (install it by typing sudo pacman -S extra/libsignal-protocol-c)
gstreamer-app-1.0, gstreamer-audio-1.0, gstreamer-rtp-1.0 and gstreamer-video-1.0 (install them by typing sudo pacman -S extra/gst-plugins-base)

1. Download git (sudo pacman -S git)
2. Clone repo (git clone https://github.com/esterOSS/echats)
3. Go into echats directory
4. Type ./configure to check if all the necessary libraries are installed and to configure the build environment (if there are missing libraries then install them from the prerequisites list for building ester Chats)
5. To build it, type make
6. To install it, type sudo make install 
7. To fix the build, so that it loads the necessary compiled libraries and prevent the loading shared libraries error when launching it, type cd /etc/ld.so.conf.d/ , then create a local.conf file with any CLI text editor (like nano) and edit the file so that it contains "/usr/local/lib" (without quotes) in the file, then save it.
8. To fix the missing icons, type sudo cp -r /home/[username]/echats/main/data/icons/scalable /usr/share/icons/hicolor
9. To run your freshly compilied build of ester Chats, type dino in the terminal or open the ester Chats icon inside of your desktop enviroment, and done!

