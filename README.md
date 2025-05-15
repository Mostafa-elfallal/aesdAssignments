# 🚀 Advanced Embedded Linux Development Projects

Welcome to my personal project repository for the [Advanced Embedded Linux Development Specialization](https://www.coursera.org/specializations/advanced-embedded-linux-development) offered by the University of Colorado Boulder on [Coursera](https://www.coursera.org/).  
This repository contains all of my work organized as **Git submodules**, covering kernel and user-space development using **Yocto**, **Buildroot**, and targeting **BeagleBone Blue** hardware.

---

## 📚 Specialization Courses

1. [✅ Linux System Programming & Introduction to Buildroot](https://www.coursera.org/learn/linux-system-programming-introduction-to-buildroot?specialization=advanced-embedded-linux-development)
2. [✅ Linux Kernel Programming & The Yocto Project](https://www.coursera.org/learn/linux-kernel-programming-yocto-project?specialization=advanced-embedded-linux-development)
3. [🔜 Embedded Systems Topics & Final Project](https://www.coursera.org/learn/linux-embedded-systems-topics-projects?specialization=advanced-embedded-linux-development)

---

## 🧠 Project Highlights

| Module                      | Description                                                                 | Status  |
|----------------------------|-----------------------------------------------------------------------------|---------|
| `char-device-driver`       | Custom Linux **character device driver** developed in kernel space          | ✅ Done |
| `socket-ipc-app`           | User-space **socket application** for IPC between processes                 | ✅ Done |
| `buildroot-setup`          | Complete **Buildroot** environment and root filesystem                      | ✅ Done |
| `yocto-minimal-layer`      | Custom **Yocto** meta-layer and recipes for minimal Linux build             | ✅ Done |
| `beaglebone-blue-project`  | Final project with Yocto on **BeagleBone Blue**, including hardware I/O     | 🏗️ In Progress |

> Each component is maintained as a Git submodule for modularity and version control.

---

## 🧰 Tech Stack

- 🐧 Embedded Linux
- 🛠️ Buildroot
- 📦 Yocto Project
- 🧩 Kernel Module Programming (char drivers)
- 🌐 Socket Programming (TCP/IP)
- 💻 BeagleBone Blue
- 🧪 Cross-compilation & Toolchains

---

## 📁 Repository Structure

```bash
📦 advanced-embedded-linux-projects
├── char-device-driver/         # Kernel module (submodule)
├── socket-ipc-app/             # User-space app (submodule)
├── buildroot-setup/            # Buildroot environment (submodule)
├── yocto-minimal-layer/        # Yocto custom layer (submodule)
├── beaglebone-blue-project/    # Final project (submodule)
└── README.md
