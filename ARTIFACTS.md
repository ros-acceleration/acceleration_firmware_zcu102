
| Artifact | Description |
|----------|-------------|
| kernel/Image_5.4.0 | Linux Kernel Image version 5.4.0 from the Xilinx fork targeting the ZCU102 (works in all boards of the same arch). More technically, FIT image including the kernel |
| kernel/Image_PREEMPT_RT_5.4.0  | Linux kernel FIT image version 5.4.0 with the PREEMPT_RT patch-5.4.10-rt4 applied (`5.4.0-rt4-xilinx-v2020.2`). |
| kernel/image.ub | FIT image including the kernel, DTB and rootfs |
| boot_scripts/boot.scr.default | boot script that provides U-boot commands to boot the default setup/kernel (works for both vanilla and PREEMPT_RT patched ones). Will NOT work for Xen-based systems. |
| boot_scripts/boot.scr.sd | simple boot script for non-Xen raw images produced with disk_image script |
| bootbin/BOOT.BIN.default  | ZynqMP boot BIN file for default setup, including vanilla and PREEMPT_RT patched kernels. |
| bootbin/BOOT.BIN.xen  | ZynqMP boot BIN file for Xen-based setups. |
| device_tree/system.dtb.default | Device-tree Blob (DTB) used for default Linux kernels (no hypervisor involved). |
| device_tree/system.dtb.xen | Device-tree Blob (DTB) used for Xen-based architectures. |
| bl31.bin | Arm trusted firmware BIN file |
| bl31.elf | Arm trusted firmware ELF file |
| pmufw.elf | pmu firmware ELF |
| pxelinux.cfg | pxelinux.cfg directory with default configuration file for pxe boot |
| initrd.cpio   | Minimalistic (only busybox) ramdisk, rootfs CPIO image  |
| rootfs.cpio.gz | Compressed rootfs CPIO image used for FIT image (image.ub) |
| rootfs.ext4 | Rootfs ext4 file with 1GB free space which can flashed to sd card ext4 partition |
| sdk.sh | Compressed version of Yocto Project SDK to develop applications. It has sysroot of the rootfs in the tar |
| u-boot.bin | U-boot bin |
| u-boot.elf | U-boot ELF |
| zynqmp_fsbl.elf | First stage bootloader ELF |
| zynqmp-qemu-arm.dtb | qemu device-tree blob file for single arch |
| zynqmp-qemu-multiarch-arm.dtb | qemu device-tree blob file for multi arch and it has information of a53 and other devices |
| zynqmp-qemu-multiarch-pmu.dtb | qemu device-tree blob file for multi arch and it has information of microblaze nodes |
| data   | Data for emulation. Created by `v++ -p -t sw_emu ...`. *This data for emulation seems to be specific for the architecture and agnostic to the application itself.*   |
| platform   | Base hardware platform. See [Vitis Embedded Base Platforms](https://www.xilinx.com/support/download/index.html/content/xilinx/en/downloadNav/embedded-platforms.html) for official ones, or their corresponding [sources](https://github.com/Xilinx/Vitis_Embedded_Platform_Source).   |


Added from other Xilinx's packages:

| Artifact | Description |
|----------|-------------|
| pmu_rom_qemu_sha3.elf | PMU kernel ELF file |
| zynqmp-arm-cosim.dtb | ZU+ PL-PS co-simulation device-tree. *Guess* |

Built artifacts that need to be patched:

| Artifact | Description |
|----------|-------------|
| lib/libfoonathan_memory-0.6.2.a | libfoonathan, required by FastRTPS. TODO, remove this DDS impl. |

Other git submodules:

| Artifact | Description |
|----------|-------------|
| ipxe | the "swiss army knife" of network booting. Supports both HTTPS and iSCSI, has a script engine for fine grained control of the boot process and can provide a command shell. |
| imagebuilder   | collection of scripts to build embedded virtualized systems with one or multiple domains. |
