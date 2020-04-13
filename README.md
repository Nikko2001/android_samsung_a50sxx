# TWRP Device tree for Samsung Galaxy A50s

## Install dependencies

```
sudo apt install -y bison build-essential g++-multilib git make python zip openjdk-8-jdk repo screen libtinfo5 libncurses5
```

## Building instructions

```
screen
mkdir -p ~/twrp && cd ~/twrp
repo init -u https://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-9.0
repo sync -j8
git clone https://github.com/samsung-galaxy-a50s/android_device_samsung_a507fn.git device/samsung/a507fn
export ALLOW_MISSING_DEPENDENCIES=true
. build/envsetup.sh
lunch omni_a507fn-eng
mka recoveryimage
```

*Note: Do not copy-paste the whole block, instead run the commands one-by-one!*

Your final image will be `recovery.img` in `~/twrp/out/target/product/a507fn/`. 

If you encounter any problems, create a Github issue. 

## Acknowledgements

TeamWin, OmniRom, TwrpBuilder, geiti94, halcyon441 (on XDA)

Copyright (c) 2019 A507FN Project and contributors. 
