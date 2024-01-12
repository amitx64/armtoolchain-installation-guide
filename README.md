### arm-none-eabi-gcc Installation Guide

This guide provides step-by-step instructions for installing `arm-none-eabi-gcc` on a Linux system.

#### Step 1: Remove Existing Installation (if any)

```bash
sudo apt remove gcc-arm-none-eabi
```

#### Step 2: Download and Extract the Latest Version

Download the latest version (Linux x86_64 Tarball) from the official website and check its MD5. Unpack it into a chosen directory (e.g., `/usr/share/`).

```bash
sudo tar xjf gcc-arm-none-eabi-YOUR-VERSION.tar.bz2 -C /usr/share/
```

#### Step 3: Create System-wide Binaries Access

```bash
sudo ln -s /usr/share/gcc-arm-none-eabi-YOUR-VERSION/bin/arm-none-eabi-gcc /usr/bin/arm-none-eabi-gcc 
sudo ln -s /usr/share/gcc-arm-none-eabi-YOUR-VERSION/bin/arm-none-eabi-g++ /usr/bin/arm-none-eabi-g++
sudo ln -s /usr/share/gcc-arm-none-eabi-YOUR-VERSION/bin/arm-none-eabi-gdb /usr/bin/arm-none-eabi-gdb
sudo ln -s /usr/share/gcc-arm-none-eabi-YOUR-VERSION/bin/arm-none-eabi-size /usr/bin/arm-none-eabi-size
sudo ln -s /usr/share/gcc-arm-none-eabi-YOUR-VERSION/bin/arm-none-eabi-objcopy /usr/bin/arm-none-eabi-objcopy
```

#### Step 4: Install Dependencies

Install dependencies based on your system. For example:

```bash
sudo apt install libncurses-dev
sudo ln -s /usr/lib/x86_64-linux-gnu/libncurses.so.6 /usr/lib/x86_64-linux-gnu/libncurses.so.5
sudo ln -s /usr/lib/x86_64-linux-gnu/libtinfo.so.6 /usr/lib/x86_64-linux-gnu/libtinfo.so.5
```

#### Step 5: Verify Installation

Check if the installation was successful by running the following commands:

```bash
arm-none-eabi-gcc --version
arm-none-eabi-g++ --version
arm-none-eabi-gdb --version
arm-none-eabi-size --version
```
