# ArchWSL
ArchLinux on WSL (Windows 10 FCU or later)
based on [wsldl](https://github.com/yuk7/wsldl)


![screenshot](https://raw.githubusercontent.com/wiki/yuk7/wsldl/img/Arch_Alpine_Ubuntu.png)

[![Travis (.org)](https://img.shields.io/travis/yuk7/ArchWSL.svg?label=%F0%9F%93%81build&style=flat-square)](https://travis-ci.org/yuk7/ArchWSL)
[![AppVeyor](https://img.shields.io/appveyor/ci/yuk7/ArchWSL.svg?logo=Windows&style=flat-square)](https://ci.appveyor.com/project/yuk7/archwsl)
[![Travis (.org)](https://img.shields.io/travis/yuk7/ArchWSL-FS.svg?logo=Linux&style=flat-square)](https://travis-ci.org/yuk7/ArchWSL)
[![Github All Releases](https://img.shields.io/github/downloads/yuk7/ArchWSL/total.svg?style=flat-square)](https://github.com/yuk7/ArchWSL/releases/latest)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
![License](https://img.shields.io/github/license/yuk7/ArchWSL.svg?style=flat-square)


### [⬇Download](https://github.com/yuk7/ArchWSL/releases/latest) | [📓Wiki](https://github.com/yuk7/ArchWSL/wiki)

## 💻Requirements
* Windows 10 1709 Fall Creators Update 64bit or later.
* Windows Subsystem for Linux feature is enabled.

## 💾Install
### 📁zip
#### 1. [Download](https://github.com/yuk7/ArchWSL/releases/latest) installer zip

#### 2. Extract all files in zip file to same directory
Please extract to a folder that has write permission.
For example 'Program Files' can not be used.

#### 3. Run Arch.exe to Extract rootfs and Register to WSL
Exe filename is using to the instance name to register.
If you rename it you can register with a different name and have multiple installs.

  **Note:** _Source code for Arch.exe can be found in [yuk7/wsldl](https://github.com/yuk7/wsldl)._

#### 4. Before using pacman, please initialize keyring
```dos
>Arch.exe
[root@PC-NAME user]# pacman-key --init

[root@PC-NAME user]# pacman-key --populate

```
### 📦appx
#### 1. [Download](https://github.com/yuk7/ArchWSL/releases/latest) installer .appx and .cer
#### 2. Install .cer to Trusted root Certificate
#### 3. Install .appx

## 📝How-to-Use(for Installed Instance)
#### exe Usage
```dos
Useage :
    <no args>
      - Launches the distro's default behavior. By default, this launches your default shell.

    run <command line>
      - Run the given command line in that distro.

    config [setting [value]]
      - `--default-user <user>`: Set the default user for this distro to <user>
      - `--default-uid <uid>`: Set the default user uid for this distro to <uid>
      - `--append-path <on|off>`: Switch of Append Windows PATH to $PATH
      - `--mount-drive <on|off>`: Switch of Mount drives

    get [setting]
      - `--default-uid`: Get the default user uid in this distro
      - `--append-path`: Get on/off status of Append Windows PATH to $PATH
      - `--mount-drive`: Get on/off status of Mount drives
      - `--lxuid`: Get LxUID key for this distro
    backup
      - Execute the backup function using tar.

    clean
      - Uninstalls the distro.

    help
      - Print this usage message.
```

## 🚫Known issues
Please see [Wiki](https://github.com/yuk7/ArchWSL/wiki).
