################################################################################
1. How to Build
        - get Toolchain
                From android git serveru, codesourcery and etc ..
                - gcc/linux-x86/aarch64/aarch64-linux-android-4.9/bin/aarch64-linux-android-

                From Qualcomm developer network (https://developer.qualcomm.com/software/snapdragon-llvm-compiler-android/tools)
                - llvm-arm-toolchain-ship/8.0/                

        - make output folder 
                EX) OUTPUT_DIR=out
                $ mkdir out

        - edit Makefile
                edit "CROSS_COMPILE" to right toolchain path(You downloaded).
                        EX)  CROSS_COMPILE=<android platform directory you download>/android/prebuilts/gcc/linux-x86/aarch64/aarch64-linux-android-4.9/bin/aarch64-linux-android-
                        Ex)  CROSS_COMPILE=/usr/local/toolchain/gcc/linux-x86/aarch64/aarch64-linux-android-4.9/bin/aarch64-linux-android- // check the location of toolchain
        - to Build
               $ ./build_kernel.sh

2. Output files
        - Kernel : arch/arm64/boot/Image
        - module : drivers/*/*.ko

3. How to Clean 
        Change to OUTPUT_DIR folder
        EX) /home/dpi/qb5_8814/workspace/P4_1716/android/out/target/product/a71/out
        $ make clean
################################################################################
