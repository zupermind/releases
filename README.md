# MCDP CLI

A command-line interface for MCDP operations.

Available for:

- Ubuntu 22/24
- Windows 11
- Mac OS X 15

Available for both ARM and x86 processors.


# Installation

## Prerequisites

A working Docker installation.

## First time installation

Install from the [Github releases](https://github.com/zupermind/mcdp-binaries/releases/latest) the executable that matches your system.
Subsequently, you can use the `update` command to update to the latest version.


## Special instructions for Linux

Download the binary.
Use

    chmod +x <file>

to make it executable.

## Special instructions for OS X

If you download the binary through the browser, the executable will be marked as tainted and the security settings will block it.

The solution is to download it using `wget` or `curl`. Example: (copy the updated link)


    curl -L -o mcdp https://github.com/zupermind/mcdp-binaries/releases/download/v2025.1.2505251826/mcdp-cli-2025.1.2505251826-macos15-arm64
    chmod +x mcdp 
    ./mcdp version


## Special instructions for Windows

If you download the binary through the browser, the executable will be marked as tainted and the security settings will block it.
The solution is to download it using `curl` or `wget` as above. Otherwise, just accept all the warnings when running the executable.


Note that the .exe file is for running natively on Windows through PowerShell. For working on WSL, you should download the appropriate binary for Ubuntu.


# Self-update

You can run the `update` command:

    mcdp-cli update 

to update to the latest version automatically. This command will overwrite the binary.