# Before starting you may do them.

## For https://cdimage.ubuntu.com/kubuntu/releases/23.10/release/kubuntu-23.10-desktop-amd64.iso

sudo apt install gcc-aarch64-linux-gnu libssl-dev

## For https://download.manjaro.org/gnome/23.1.3/manjaro-gnome-23.1.3-minimal-240113-linux66.iso

sudo pacman -S aarch64-linux-gnu-gcc

### Set proton-clang

cd

git clone https://github.com/kdrag0n/proton-clang.git --depth 1

export export PATH=$PATH:~/proton-clang/bin

export CROSS_COMPILE=aarch64-linux-gnu-

export CROSS_COMPILE_ARM32=arm-linux-gnueabi-

export ARCH=arm64

export CC=clang

### Set android_kernel_xiaomi_msm8953

cd

git clone https://github.com/xiaomi-msm8953-devs/android_kernel_xiaomi_msm8953.git --depth 1

### Build kernel for sakura

cd

cd android_kernel_xiaomi_msm8953

make ARCH=arm64 CC=clang O=out msm8953-perf_defconfig

make ARCH=arm64 O=out CC=clang -j8
