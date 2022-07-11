# realsence

> https://github.com/haohaoalt/librealsense.git

```bash
sudo apt install libglfw3-dev libgl1-mesa-dev libglu1-mesa-dev libusb-1.0-0-dev
mkdir -p ~/repos && cd ~/repos
git clone https://github.com/IntelRealSense/librealsense
mkdir -p librealsense/build && cd librealsense/build
cmake .. -DFORCE_RSUSB_BACKEND=true -DCMAKE_BUILD_TYPE=release
make -j$(nproc)
sudo make install

# You'll need to copy or symlink udev rules prior to using the camera:

sudo ln -s ~/repos/librealsense/config/99-realsense-libusb.rules /etc/udev/rules.d/99-realsense-libusb.rules
```

```bash
realsense-viewer
```