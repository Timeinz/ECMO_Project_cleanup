
For building anything make sure to have get the submodules (eg. clone
recursively) like FreeRTOS and the pico-sdk.

it is assumed you are building from Linux. (easier than windows in my
experrience)

you need:
build-essentials
cmake
ninja-build

and the toolchain:
gcc-arm-none-eabi
libnewlib-arm-none-eabi
libstdc++-arm-none-eabi-newlib

also recommended to build picotool (optional):
cd external/picotool
mkdir build && cd build
cmake .. -DPICO_SDK_PATH=$(pwd)/../../pico-sdk
cmake --build . -j$(nproc)
cmake --install . --prefix ../install
