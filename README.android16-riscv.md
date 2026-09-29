# A16_RISCV/hardware/baylibre/usb: android16-riscv

Changes made for the Android 16 (AOSP, riscv64) bring-up of the BananaPi BPI-F3 (SpacemiT K1) and the BananaPi BPI-SM10 (SpacemiT K3), on branch `android16-riscv`.

USB HAL sepolicy.

## Changes

- **sepolicy: declare sysfs_typec_vendor for older vendor API levels**: sysfs_typec is only in the platform public policy on ToT; vendor policy built against the frozen 202504 API needs its own type name. Document why the HAL uses the platform sysfs_typec on newer API levels.

## Build

```
./build.sh k1   # BPI-F3 (K1): kernel, bootloaders and Android images
./build.sh k3   # BPI-SM10 (K3), not booted yet
```

`./build.sh --help` lists the options (`--skip-kernel`, `--kernel-only`, ...).
