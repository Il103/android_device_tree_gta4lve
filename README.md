# Samsung Galaxy Tab A7 10.4 (SM-T509) - gta4lve

## Device specifications

| Feature | Spec |
|---|---|
| Chipset | Unisoc T618 (UMS512) |
| CPU | Octa-core (2x Cortex-A75 2.0 GHz + 6x Cortex-A55 1.8 GHz) |
| GPU | Mali-G52 MP2 |
| RAM | 3 GB |
| Storage | 32 GB |
| Display | 10.4" TFT, 1200x2000 |
| Battery | 7040 mAh |
| Android | 12 (Stock), LineageOS 23 (Target) |
| Kernel | 4.14.199 (Unisoc BSP) |
| Architecture | arm64 |

## Device picture

![Samsung Galaxy Tab A7 10.4 (2022)](https://fdn2.gsmarena.com/vv/pics/samsung/samsung-galaxy-tab-a7-104-2022-1.jpg)

## Build instructions

```bash
repo init -u https://github.com/LineageOS/android.git -b lineage-23.2 --depth=1
repo sync -c -j$(nproc --all)

# Clone device trees
git clone https://github.com/Il103/android_device_tree_gta4lve.git device/samsung/gta4lve -b device-lineage-23.2
git clone https://github.com/Il103/android_vendor_tree_gta4lve.git vendor/samsung/gta4lve -b vendor-lineage-23.2
git clone https://github.com/Il103/android_kernel_samsung_gta4lve.git kernel/samsung/gta4lve -b kernel-lineage-23.2

# Build
source build/envsetup.sh
lunch lineage_gta4lve-userdebug
mka bacon -j$(nproc --all)
```

## Status

| Component | Status |
|---|---|
| Boot | Not tested |
| WiFi | Not tested |
| Bluetooth | Not tested |
| Camera | Not tested |
| Audio | Not tested |
| Cellular | N/A (WiFi only) |
| Touchscreen | Not tested |
| GPS | Not tested |

## Credits

- [BERU](https://github.com/Il103) for building and maintaining this device tree
- LineageOS for the build system
