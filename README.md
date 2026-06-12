# JLQ JR510 POCO C40 Live Dump

This repository contains a live dump of the **POCO C40** (codename `frost`) based on the **JLQ JR510** chipset. The purpose is to provide developers with all necessary files to recreate device tree, build TWRP/OrangeFox, develop a custom kernel, or improve GSI compatibility.

## ⚠️ Disclaimer
- These files were obtained through reverse engineering from the device itself (live dump) and from official fastboot firmware.
- The kernel is subject to **GPLv2**. The original manufacturer (JLQ / Xiaomi) has not released kernel sources, violating GPL. This dump is a clean-room effort to help the community.

## 📁 Contents (planned / partially available)
- `vmlinux` – uncompressed kernel ELF with symbols (from firmware)
- `config.gz` – kernel configuration
- `kallsyms` – symbol table (after root)
- `dmesg.log` – kernel boot log
- `dtb/` – device tree blobs (from `vendor_boot.img`)
- `dtbo/` – device tree overlays
- `boot/` – unpacked `boot.img` (kernel + ramdisk)
- `logs/` – `logcat`, `getprop`, etc.

## 🛠 How to use
1. Clone this repo.
2. Use `dtc` to decompile `.dtb` → `.dts`.
3. Load `vmlinux` into Ghidra/IDA Pro with symbols.
4. Use `twrpdtgen` or manual device tree creation.
5. Build TWRP/OrangeFox or custom kernel.

## 🙌 Credits
- Dumped and organized by **Ckicker**
- Thanks to the POCO C40 community for motivation.

## 📜 License
- Kernel-related files are under **GPLv2** (see LICENSE file).
- Other files are provided as-is for educational purposes.
