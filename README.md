# Advanced Embedded Linux Development

Coursework for the [Advanced Embedded Linux Development Specialization](https://www.coursera.org/specializations/advanced-embedded-linux-development) (University of Colorado Boulder, Coursera).

Each assignment lives in its own repository under the course's GitHub organisation and is included here as a Git submodule. Every assignment builds on the previous one, so the later repositories also contain the earlier code.

## Courses

1. [Linux System Programming and Introduction to Buildroot](https://www.coursera.org/learn/linux-system-programming-introduction-to-buildroot)
2. [Linux Kernel Programming and the Yocto Project](https://www.coursera.org/learn/linux-kernel-programming-yocto-project)
3. [Embedded Systems Topics and Final Project](https://www.coursera.org/learn/linux-embedded-systems-topics-projects). The final project is a Yocto BSP with kernel sensor drivers for the BeagleBone Blue: [BBBlue-BSP](https://github.com/Mostafa-elfallal/BBBlue-BSP).

## Assignments

| Submodule | Work |
|---|---|
| `assignment1` | Shell scripts (`finder.sh`, `writer.sh`) and the test setup used by later assignments |
| `assignment2` | `writer` rewritten in C with a Makefile, cross-compiled for ARM64 |
| `assignment3` | System calls (`fork`, `exec`, `wait`) and POSIX threads; `manual-linux.sh` builds an ARM64 kernel and a BusyBox root filesystem from source and boots them on QEMU |
| `assignment4` | The same system built with Buildroot: `BR2_EXTERNAL` tree, custom package and defconfig, SSH access, tests run inside the QEMU image |
| `assignment5` | `aesdsocket`: a TCP server in C that runs as a daemon, appends received data to a file and returns it to the client, with clean shutdown on `SIGINT`/`SIGTERM` |
| `assignment6` | Build moved to Yocto with a custom `meta-aesd` layer and image; `aesdsocket` made multithreaded (one thread per client, mutex-protected file access, periodic timestamps) |
| `assignment7` | Kernel modules from *Linux Device Drivers, 3rd Edition* (`scull`, `faulty`) and the related example modules, built and loaded in the target image |
| `assignment8` | `aesdchar`: a character device driver backed by a circular buffer, with locking and dynamic allocation; recipes for the out-of-tree modules and init scripts to load them |
| `assignment9` | `llseek` and an `AESDCHAR_IOCSEEKTO` `ioctl` in the driver, used by `aesdsocket` to seek within the device |

The driver and socket server source is in `assignment3` (the `assignments-3-and-later` repository), under `aesd-char-driver/` and `server/`. `server/valgrind-out.txt` shows the server running with no leaks.

Most assignments are checked automatically in GitHub Actions by the course test scripts (`full-test.sh`, `unit-test.sh`).

## Cloning

```sh
git clone --recurse-submodules https://github.com/Mostafa-elfallal/aesdAssignments.git
```
