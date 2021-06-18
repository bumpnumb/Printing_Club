
# Forgot to take images of the prints when disassembled. Sorry!


This is a small mount for a raspberry pi + camera v2 that fits on the e3d toolchanger.
Will fit on any extrusion with 8mm spacing.


Do not mount pi untill after the mount_rear is fastened on the extrusion, screws cannot be accesed after pi is mounted.
Links can be printed if camera needs to be further extended, do note the length of pi camera bus cable.




HOWTO:
create picam-stream.sh on pi [Link](https://gist.github.com/russfeld/0878b1f8eaf7409136b9125ce5e1458f)
 - Write stream key and prefered RTMP endpoint

Install ffmpeg:
Install h264 library

    Open a terminal window on the raspberrypi (or via SSH connection) and type in the following commands:
    Download h264 library: git clone --depth 1 https://code.videolan.org/videolan/x264
    Change directory to the x264 folder: cd x264
    Configure installation: ./configure --host=arm-unknown-linux-gnueabi --enable-static --disable-opencl
    Create the installation: make -j4
    Install h264 library on your system: sudo make install

Install ffmpeg with h264

    Change to home directory: cd ~
    Download ffmpeg: git clone git://source.ffmpeg.org/ffmpeg --depth=1
    Change to ffmpeg directory: cd ffmpeg
    Configure installation: ./configure --arch=armel --target-os=linux --enable-gpl --enable-libx264 --enable-nonfree
    Make the installation: make -j4. Note this step will take a long time!
    Now finally run the installation: sudo make install


raspivid might need to be installed.