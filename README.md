### How to compile 
* [Init AOSP Compile Env](https://source.android.com/setup)
* Init Source `repo init -u https://android.googlesource.com/platform/manifest -b android-7.1.2_r28`
* Replace ADB Source Code
```bash
git clone https://github.com/lxs137/aosp-core-adb.git 
cd aosp-core-adb 
git checkout android-7.1.2_r28
cp -r ./adb <AOSP_DIR>/system/core/adb
```
* Compile Adb Daemon (x86 32bit)
```bash
export AOSP7_HOME=/path/to/aosp/7
. build/envsetup.sh
lunch aosp_x86-eng 
make out/target/product/generic_x86/root/sbin/adbd
```
* Compile Adb Host (linux x86)
```bash
export AOSP7_HOME=/path/to/aosp/7
. build/envsetup.sh
lunch aosp_x86-eng 
make out/host/linux-x86/bin/adb
```
