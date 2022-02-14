# ProtonAOSP

ProtonAOSP is a minimal custom Android ROM focused on UI/UX and performance, with a touch of security and privacy. It is based on [Android Open Source Project (AOSP)](https://source.android.com/).

## Getting source code

First, make sure you have an [Android build environment](https://source.android.com/setup/build/initializing) and the [repo tool](https://source.android.com/setup/build/downloading) set up. After that, run the following commands:

```
repo init -u https://github.com/ProtonAOSP-Plus/manifest -b sc
```
```
repo sync -j$(nproc --all) --force-sync --no-tags --no-clone-bundle --prune --optimized-fetch
```
```
source build/envsetup.sh
lunch aosp_device-buildtype
make otapackage
```

This is a large download that will take approximately 100 GB of disk space, so plan accordingly.


Good luck!
