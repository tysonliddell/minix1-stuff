# minix1-stuff
## Original MINIX disks
The original MINIX 1.1 disks are contained in `Intel-1.1.tar.gz`. From the
MINIX 1.1 README:

```
Disk 1: Boot Disk
Disk 2: Root File System
Disk 3: /usr
Disk 4: /user
Disk 5: Kernel, H and Include Sources
Disk 6: FS and Lib Sources
Disk 7: MM and Tools Sources
Disk 8: Commands Sources
```

## Source disks
To set up a MINIX 1.1 development environment, as explained in Tanenbaum's
*Operating Systems: Design and Implementation* first edition, multiple source
disks are required. One disk for each directory in the MINIX source code:

```
kernel
mm
fs
h
lib
tools
commands
test
include
```

Following the somewhat tedious process outlined in the MINIX book results in
the nine source disks in `source-disks.tar.gz`. Each disk is stored in the 86F
disk image format (a low-level FM/MFM flux format) making it easy to use 86Box
as a dev environment with accurate, low-level disk emulation.

## 86Box setup
An IBM XT with two 5.25" double-sided, double-density floppy drives was chosen
as the dev environment to follow Tanenbaum's MINIX 1 book closely.

```
[Machine]
cpu_family = 8088
cpu_multi = 1
cpu_speed = 4772728
cpu_use_dynarec = 0
machine = ibmxt86
mem_size = 640

[Video]
gfxcard = mda

[Input devices]
keyboard_type = keyboard_pc_xt
mouse_type = none

[Floppy and CD-ROM drives]
fdd_01_check_bpb = 0
fdd_02_check_bpb = 0

[IBM XT (1986)]
bios = ibm5160_050986
enable_5161 = 1

[IBM MDA]
rgb_type = 1
font = 0
```
