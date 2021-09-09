# acceleration_firmware_zcu102

| Board | Picture | Description |
|------------|-------|-------------|
| [Xilinx Zynq UltraScale+ MPSoC ZCU102 Evaluation Kit (`ZCU102`)](https://www.xilinx.com/products/boards-and-kits/ek-u1-zcu102-g.html) | ![](https://www.xilinx.com/content/dam/xilinx/imgs/kits/whats-inside/zcu102-evaluation-board-w.jpg) | The ZCU102 Evaluation Kit enables designers to jumpstart designs for automotive, industrial, video, and communications applications. This kit features a Zynq® UltraScale+™ MPSoC with a quad-core Arm® Cortex®-A53, dual-core Cortex-R5F real-time processors, and a Mali™-400 MP2 graphics processing unit  | 

This repository provides Xilinx's firmware artifacts for the ZCU102 board meant to accelerate ROS 2 robotic applications.

<ins>**NOTE**</ins>: *This repository is has various **GB** of data. Due to GitHub size restrictions, the whole source code is available under [releases](https://github.com/ros-acceleration/acceleration_firmware_zcu102/releases)*. *Refer to each corresponding's release `firmware/ARTIFACTS.md` file for a description of all the artifacts included*.

## Hardware Acceleration capabilities

According to [REP-2008's proposal](https://github.com/ros-infrastructure/rep/pull/324).

| Capability | Status |
|------------|--------|
| **`1.` Kernel Levels** | |
| [`1.i` level I kernels](https://ros.org/reps/rep-2008.html#i) | ✓ |
| [`1.ii` level II kernels](https://ros.org/reps/rep-2008.html#ii) | :warning: |
| [`1.iii` level III kernels](https://ros.org/reps/rep-2008.html#iii) |  |
| **`2.` Build System** | |
| [`2.i` ament extensions](https://ros.org/reps/rep-2008.html#id13) | ✓ |
| [`2.ii` `ament_acceleration` support](https://ros.org/reps/rep-2008.html#id14) | |
| **`3`. Build Tools** | |
| [`3.i` hardware emulation (`hw_emu`) ](https://ros.org/reps/rep-2008.html#id15) | ✓ |
| [`3.ii` hardware emulation (`sw_emu`)](https://ros.org/reps/rep-2008.html#id16) | ✓ |
| [`3.iii` image tooling](https://ros.org/reps/rep-2008.html#id17) | ✓ |
| [`3.iv` Linux kernel ](https://ros.org/reps/rep-2008.html#iv) | ✓ |
| [`3.iv.a` modern Linux kernel](https://ros.org/reps/rep-2008.html#iv-a) | ✓ |
| [`3.iv.b` LTS Linux kernel](https://ros.org/reps/rep-2008.html#iv-b) | |
| [`3.v` hypervisor ](https://ros.org/reps/rep-2008.html#v) | ✓ |
| [`3.v.a` no control domain VMs](https://ros.org/reps/rep-2008.html#v-a) | ✓ |
| [`3.v.b` guest VMs in disk](https://ros.org/reps/rep-2008.html#v-b) | ✓ |
| [`3.v.c` control domain in disk](https://ros.org/reps/rep-2008.html#v-c) | ✓  |
| [`3.v.d` no control domain VMs in disk](https://ros.org/reps/rep-2008.html#v-d) | |
| [`3.vi` network booting ](https://ros.org/reps/rep-2008.html#vi) | |
| [`3.vi.a` boot artifacts ](https://ros.org/reps/rep-2008.html#vi-a) | |
| [`3.vi.b` rootfs ](https://ros.org/reps/rep-2008.html#vi-b) | |
| [`3.vi.c` multi-network boot](https://ros.org/reps/rep-2008.html#vi-c) | |
| [`3.vi.d` secure network booting](https://ros.org/reps/rep-2008.html#vi-d) | |
| [`3.vi.e` save in disk network boot](https://ros.org/reps/rep-2008.html#vi-e) | |
| **`4.` Benchmarking** | |
| [`4.i` kernel benchmarking](https://ros.org/reps/rep-2008.html#id18) | ✓ |
| [`4.ii` ROS 2 acceleration benchmarking](https://ros.org/reps/rep-2008.html#id19) | |
| **`5.` Documentation** | |
| [`5.i` in-code documentation](https://ros.org/reps/rep-2008.html#id20) | ✓ |
| **`6.` Testing and CI** | |
| [`6.i` `acceleration_examples` ](https://ros.org/reps/rep-2008.html#id21) | ✓ |


### Quality Declaration

No quality is claimed according to [REP-2004](https://www.ros.org/reps/rep-2004.html). This package should only be used in workstations to produced valid firmware for the targeted hardware.
