## Getting source code

First, make sure you have an [Android build environment](https://source.android.com/setup/build/initializing) and the [repo tool](https://source.android.com/setup/build/downloading) set up. After that, run the following commands:

```
repo init -u https://github.com/ProtonPlus-ORG/manifest -b tm-qpr2
```

```
repo sync -j$(nproc --all) --force-sync --no-tags --no-clone-bundle --prune --optimized-fetch
```

```
source build/envsetup.sh
lunch device-buildtype
m otapackage
```

This is a large download that will take approximately 100 GB of disk space, so plan accordingly.

Good luck!
