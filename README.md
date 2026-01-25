# AmazeGaming 🚀

**AmazeGaming** is a lightweight C# utility designed for real-time automatic optimization of gaming processes. It dynamically allocates system resources, minimizes input lag, and prioritizes the active gaming window to ensure peak performance.

## Core Features

The application applies a comprehensive suite of 8 key optimizations to the active process:

* **CPU Affinity**: Automatically binds the process to specific physical cores to reduce scheduler overhead and latency.
* **High Priority**: Elevates the process priority to "High" (High Priority Class) within the Windows kernel.
* **High Resolution Timer**: Forces the system timer resolution to 0.5ms (via `NtSetTimerResolution`) for maximum input responsiveness.
* **MMCSS (Multimedia Class Scheduler)**: Registers threads into the "Games" profile for prioritized data processing.
* **Power Throttling Disable**: Prevents Windows from limiting power to the active process for energy-saving purposes.
* **Memory Page Priority**: Increases the memory page priority within RAM to prevent paging of critical game data.
* **Priority Boost Disable**: Disables dynamic priority decay, ensuring Windows does not lower the process priority over time.
* **DwmGhosting Disable**: Prevents the "ghosting" or freezing of the game window interface under heavy load.

## Installation

1. Download the latest release: `AmazeGaming_Setup.exe`.
2. Run the installer (available in English, Russian, Ukrainian, and Turkish).
3. Post-installation, the program automatically registers itself in the **Windows Task Scheduler** with `Highest Privileges` to ensure it starts with the system.

## How It Works

AmazeGaming runs as a background service monitoring the **Foreground Window**. When you switch to a game:
1. It verifies the process is not on the **Blacklist** (e.g., Explorer, Chrome, etc.).
2. It immediately applies all 8 optimization tweaks to the active process.
3. When you switch windows, resources are dynamically redistributed to maintain system stability.

## System Requirements

* **OS**: Windows 10 / 11 (x64)
* **Privileges**: Administrator rights required (for kernel-level interaction and Task Scheduler access).
* **Dependencies**: .NET Framework 4.8.

## Technologies Used

* **C# / .NET 4.8**
* **Win32 API / ntdll.dll** (Low-level system calls)
* **WinRing0** (Kernel-level driver access library)

## Disclaimer

This software is designed for system optimization. The author is not responsible for any system instability or actions taken by third-party anti-cheat software. Use at your own risk.

---
Created by **amazingb01** & **adiru3**

## 🔗 Connect with me

[![YouTube](https://img.shields.io/badge/YouTube-@adiruaim-FF0000?style=for-the-badge&logo=youtube)](https://www.youtube.com/@adiruaim)
[![TikTok](https://img.shields.io/badge/TikTok-@adiruhs-000000?style=for-the-badge&logo=tiktok)](https://www.tiktok.com/@adiruhs)
[![Donatello](https://img.shields.io/badge/Support-Donatello-orange?style=for-the-badge)](https://donatello.to/Adiru3)
