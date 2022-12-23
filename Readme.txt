Realme 7 Pro kernel
coming soon

Kernel compile Guide 

export ARCH=arm64
export SUBARCH=arm64
export HEADER_ARCH=arm64
PATH="&ltPATH TO CLANG FOLDER&gt/BIN:&ltPATH TO GCC 64 bit FOLDER&gt/BIN:&ltPATH TO GCC 32 bit FOLDER&gt/BIN${PATH}"
rm -rf out
make O=out clean && make mrproper
make O=out ARCH=arm64 (device defconfig)
make -j$(nproc --all) O=out ARCH=arm64 CC=clang CLANG_TRIPLE=aarch64-linux-gnu- CROSS_COMPILE=aarch64-linux-android- CROSS_COMPILE_ARM32=arm-linux-androideabi-
 
 
if you get stuck, let me know


 Clang Compiler         :- https://android.googlesource.com/platform/prebuilts/clang/host/linux-x86/+/ee5ad7f5229892ff06b476e5b5a11ca1f39bf3a9/clang-r365631c/
 GCC 64 bit compiler    :- https://android.googlesource.com/platform/prebuilts/gcc/linux-x86/aarch64/aarch64-linux-android-4.9/+/refs/tags/android-11.0.0_r48


