ubuntu1604

http://releases.linaro.org/archive/14.09/components/toolchain/binaries/gcc-linaro-aarch64-linux-gnu-4.9-2014.09_linux.tar.xz

http://dn.odroid.com/toolchains/gcc-linaro-arm-none-eabi-4.8-2014.04_linux.tar.xz

http://dn.odroid.com/toolchains/gcc-linaro-aarch64-none-elf-4.9-2014.09_linux.tar.xz

repo init -u https://github.com/WalkerWaqi/android.git -b s905_6.0.1_master

repo sync

repo start s905_6.0.1_master --all


export ARCH=arm64

export CROSS_COMPILE=aarch64-linux-gnu-

export PATH=/opt/gcc-linaro-aarch64-linux-gnu-4.9-2014.09_linux/bin:$PATH

export PATH=/opt/gcc-linaro-arm-none-eabi-4.8-2014.04_linux/bin:$PATH

export JAVA_HOME=/usr/lib/jvm/java-1.7.0-openjdk-amd64

export PATH=$JAVA_HOME/bin:$PATH


source build/envsetup.sh

lunch odroidc2-eng-32

make -j4 selfinstall
