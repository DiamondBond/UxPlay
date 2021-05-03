This project is an early stage prototype of unix AirPlay server.
Work is based on https://github.com/antimof/UxPlay with the following PR's merged (& some code style cleanup):
https://github.com/antimof/UxPlay/pull/42
https://github.com/antimof/UxPlay/pull/31

## Features

1. Based on Gstreamer.
1. Video and audio are supported out of the box.
1. Gstreamer decoding is plugin agnostic. Uses accelerated decoders if availible. VAAPI is preferable.
1. Automatic screen orientation.

## Building

```bash
sudo apt-get install cmake
sudo apt-get install libssl-dev libavahi-compat-libdnssd-dev \
                     libgstreamer1.0-dev libgstreamer-plugins-base1.0-dev \
                     gstreamer1.0-libav
sudo apt-get install gstreamer1.0-vaapi # For Intel graphics
mkdir build
cd build
cmake ..
make
```
