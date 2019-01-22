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
