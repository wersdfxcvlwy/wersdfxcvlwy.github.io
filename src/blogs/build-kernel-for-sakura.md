# Build kernel for sakura

## Set proton-clang
### `cd `
### `git clone https://github.com/kdrag0n/proton-clang.git --depth 1`
### `export export PATH=$PATH:~/proton-clang/bin`
### `export CROSS_COMPILE=aarch64-linux-gnu-`
### `export CROSS_COMPILE_ARM32=arm-linux-gnueabi-`
### `export ARCH=arm64`
### `export CC=clang`

## Set android_kernel_xiaomi_msm8953
### `cd`
### `git clone https://github.com/xiaomi-msm8953-devs/android_kernel_xiaomi_msm8953.git --depth 1`

## Build kernel for sakura
### `cd`
### `cd android_kernel_xiaomi_msm8953`
### `make ARCH=arm64 CC=clang O=out msm8953-perf_defconfig`
### `make ARCH=arm64 O=out CC=clang -j8`