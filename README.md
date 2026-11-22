# Light Phone III kernel

Android 12 GKI 5.10.198, based on `android12-5.10-2024-01_r3`.
Requires vendor modules extracted from stock LP3 firmware.

```sh
mkdir lp3-kernel && cd lp3-kernel
repo init -u https://github.com/dtingley11/android_kernel_light_LightPhoneIII -b main -m lp3-manifest.xml --manifest-depth=1 --depth=1
repo sync -c -j4
BUILD_CONFIG=common/build.config.gki.aarch64 build/build.sh -j16
```

Kernel output: `out/android12-5.10/dist/Image`.
