# android_device_anbernic_rg351

The purpose of this project is to make a lineageos image of rg351p/v. 

You need initialize your local repository using the LineageOS trees, use a command like this:
```
repo init -u git://github.com/LineageOS/android.git -b lineage-18.1
repo sync
```

It takes a lot of time and space to to download.

After that's done, go into the **device** folder in the lineage source and clone the **android_device_anbernic_rg351** repo, then rename the folder to **anbernic**.

Then go back to the repo sync's folder, create a **kernel** folder. then in that kernel folder, create an folder named  **anbernic**. Then in that folder, clone **android_kernel_anbernic_rg351**, and then rename it to **rg351**.

After that,it's the standard android build instructions.

```
source build/envsetup.sh
lunch lineage_rg351p-userdebug
make -j8 bootimage systemimage vendorimage
```
Then, Run that as root and there is a script called **mkimg.sh** in device folder to make an sdcard image.

# Related Links

LineageOS (https://github.com/LineageOS/android)

Devices (https://github.com/turtleletortue/android_device_anbernic_rg351)

Kernel (https://github.com/turtleletortue/android_kernel_anbernic_rg351)
