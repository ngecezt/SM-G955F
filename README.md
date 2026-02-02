################################################################################
1. How to Build <br>
        - get Toolchain<br>
                From android git server, codesourcery and etc ..<br>
                - gcc-cfp/gcc-cfp-jopp-only/aarch64-linux-android-4.9/bin/aarch64-linux-android-<br>
        - edit Makefile<br>
                edit "CROSS_COMPILE" to right toolchain path(You downloaded).<br>
                        EX)  CROSS_COMPILE=<android platform directory you download>/android/prebuilts/gcc-cfp/gcc-cfp-jopp-only/aarch64-linux-android-4.9/bin/aarch64-linux-android-<br>
                        EX)  CROSS_COMPILE=/usr/local/toolchain/gcc-cfp/gcc-cfp-jopp-only/aarch64-linux-android-4.9/bin/aarch64-linux-android- // check the location of toolchain<br>
        - to Build<br>
                $ export ANDROID_MAJOR_VERSION=p<br>
                $ make ARCH=arm64 exynos8895-dream2lte_defconfig<br>
                $ make ARCH=arm64<br>
<br>
2. Output files<br>
        - Kernel : arch/arm64/boot/Image<br>
        - module : drivers/*/*.ko<br>
<br>
3. How to Clean<br>
        $ make clean<br>
################################################################################
