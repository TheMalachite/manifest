# mtk-watch #

### Setup build enviroment ###
https://source.android.com/setup/build/initializing#installing-required-packages-ubuntu-1804

### Sync ###

```bash

# Initialize local repository
repo init -u https://github.com/TheMalachite/manifest -b t-alps-q0.mp1-V9.122.1

# Sync
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

### Build ###

```bash

$ python vendor/mediatek/proprietary/scripts/releasetools/split_build_helper.py full_k39tv1_64_bsp-userdebug

```

The above command will give you 3 commands that are customized for the product and eng/userdebug/user you specfied

Note: Atleast on mt6739 building with eng made the device almost unusable due to the lag.
