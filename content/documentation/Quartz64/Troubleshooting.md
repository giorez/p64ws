---
title: "Troubleshooting"
draft: false
menu:
  docs:
    title:
    parent: "Quartz64"
    identifier: "Quartz64/Troubleshooting"
    weight: 5
---

## Stability/Boot Issues With Missing Battery Shunt

If there is no battery plugged into the board, the jumper labelled "ON/OFF_BATT" must be in place. If this is set wrong, stability issues such as failures to boot will occur.

{{< admonition type="note" >}}
 This affects only Model A
{{< /admonition >}}

## No Ethernet Connectivity

Make sure the kernel is built with `CONFIG_MOTORCOMM_PHY` set to `y`. Building it as a module (`m`) and then relying on module auto-loading is unlikely to work, because if the generic PHY driver is built in it will bind to the PHY first, unless you include the motorcomm module in your initramfs.

Note: Starting with [Debian’s `6.1~rc3-1~exp1` kernel](https://salsa.debian.org/kernel-team/linux/-/merge_requests/551) the module is included, but set to `m` and I (Diederik) have verified that it gets included in the initramfs and **works** on Model-A and Model-B with the [Quartz64](/documentation/Quartz64/Software/Releases/#plebian) images.

## "Model A" Acrylic Case Doesn't Fit

The Quartz64 does not really fit onto the bottom plate of the [Model A Acrylic Open Enclosure](/documentation//Accessories/Cases/Model_A_Acrylic_Open_Enclosure). This is because the "Mic" connector at the bottom of the board interferes with one of the posts. A workaround is to find out which post that is (you have a 50% chance of guessing it right, accounting for rotating the board) and then filing away the corner of the post pointing inwards by a few millimeters.

{{< figure src="/documentation/images/Quartz64-audio-jack-spacer-issue.jpg" width="400" >}}

An alternate solution may be to place plastic spacers with a smaller outer diameter in between the acrylic bottom plate posts and the SBC board.

## No GPU Acceleration with Debian "Bullseye" Userland

Debian Bullseye ships a Mesa version that is too old to contain the required patches for the RK356x SoC’s GPU. Upgrade to Bookworm.

## Wireless Connectivity Doesn't Work

ROCKPro64 wireless module may have CYW43455 or CYW43456 chips on board (not sure if this is the same for Quartz64 model B). Both chips are supported by `brcmfmac` Wi-Fi driver and `btbcm` Bluetooth driver.

For CYW43455 drivers attempt to load `/lib/firmware/brcm/brcmfmac43455-sdio.bin` for Wi-Fi and `/lib/firmware/brcm/BCM4345C0.hcd` for Bluetooth. Corresponding firmware files for CYW43456 are `/lib/firmware/brcm/brcmfmac43456-sdio.bin` and `/lib/firmware/brcm/BCM4345C5.hcd`.

On Manjaro firmware files for both Bluetooth and Wi-Fi on CYW43456 on are provided by `ap6256-firmware` package (`pacman -S ap6256-firmware`).

However for CYW43455 wi-fi firmware is in the `linux-firmware` package and bluetooth is in the `firmware-raspberrypi` (`pacman -S linux-firmware firmware-raspberrypi`). `linux-firmware` package is missing device specific symlinks for quartz64-a. To create them execute:

```console
# ln -s brcmfmac43455-sdio.bin /lib/firmware/brcm/brcmfmac43455-sdio.pine64,quartz64-a.bin
# ln -s brcmfmac43455-sdio.AW-CM256SM.txt /lib/firmware/brcm/brcmfmac43455-sdio.pine64,quartz64-a.txt
```

As of 2022-10-19 device tree in mainline kernel for Quartz64 model A has wrong configuration for the Bluetooth driver. [Patch](https://patchwork.kernel.org/project/linux-rockchip/patch/20220926125350.64783-1-leo@nabam.net/) is submitted to the LKML and accepted and included upstream in 6.1-rc7. It’s possible to modify dtb file provided by the current kernel using device tree compiler to enable Bluetooth or perform `make dtbs` in the patched kernel tree to get updated dtb file (`arch/arm64/boot/dts/rockchip/rk3566-quartz64-a.dtb`). Issue manifests itself with following errors in `dmesg`:

```
command 0x0c03 tx timeout
Bluetooth: hci0: BCM: Reset failed (-110)
```