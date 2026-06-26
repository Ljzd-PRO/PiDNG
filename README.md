PiDNG
=========
![](https://img.shields.io/badge/Version-4.0.9-green.svg)

Create Adobe DNG RAW files using Python.

<!-- ![](docs/demo.jpg) -->

**Features**
------------

- 8,10,12,14,16-bit precision
- Lossless compression
- DNG Tags ( extensible )

### Works with any **Bayer RAW** Data including native support for **Raspberry Pi cameras**.
- OV5467 ( Raspberry Pi Camera Module V1 )
- IMX219 ( Raspberry Pi Camera Module V2 )
- IMX477( Raspberry Pi High Quality Camera )

<!-- *Raspberry Pi High Quality Camera examples below ( DNG top, JPEG bottom )* -->

<!-- ![](docs/collage.jpg) -->

***

Instructions
------------

Requires: 
- Python3 
- Numpy  

### Install

From PyPI:
```
python3 -mpip install PiDNG 
```

Latest version from GitHub:

```
python3 -mpip install git+https://github.com/Ljzd-PRO/PiDNG.git
```

### Prebuilt wheels from GitHub Releases

This repository uses GitHub Actions to build wheels in the cloud for Linux,
macOS, and Windows. Maintainers can run the `Release wheels` workflow with a
standard tag such as `v4.0.9`; the workflow builds the wheels and uploads the
standard `.whl` files directly to the matching GitHub Release.

Developers who do not want to build the C extension locally can download a
prebuilt wheel from the published release page:

```
https://github.com/Ljzd-PRO/PiDNG/releases/tag/v4.0.9
```

Choose the file that matches your Python version and platform, then install it:

```
python3 -mpip install https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/<wheel-file-name>.whl
```

For example:

```
python3 -mpip install https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp312-cp312-win_amd64.whl
```

Wheel filename guide:
- Python 3.9 uses `cp39-cp39`
- Python 3.10 uses `cp310-cp310`
- Python 3.11 uses `cp311-cp311`
- Python 3.12 uses `cp312-cp312`
- Python 3.13 uses `cp313-cp313`
- Python 3.14 uses `cp314-cp314`
- Linux users should usually choose `manylinux`; Alpine Linux users should choose `musllinux`
- Windows 64-bit users should choose `win_amd64`; Windows 32-bit users should choose `win32`
- Apple Silicon Macs should choose `macosx_11_0_arm64`; Intel Macs should choose `macosx_*_x86_64`

After the `v4.0.9` release has been published, these direct links are available:

#### Windows

- [pidng-4.0.9-cp39-cp39-win_amd64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp39-cp39-win_amd64.whl)
- [pidng-4.0.9-cp310-cp310-win_amd64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp310-cp310-win_amd64.whl)
- [pidng-4.0.9-cp311-cp311-win_amd64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp311-cp311-win_amd64.whl)
- [pidng-4.0.9-cp312-cp312-win_amd64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp312-cp312-win_amd64.whl)
- [pidng-4.0.9-cp313-cp313-win_amd64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp313-cp313-win_amd64.whl)
- [pidng-4.0.9-cp314-cp314-win_amd64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp314-cp314-win_amd64.whl)
- [pidng-4.0.9-cp39-cp39-win32.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp39-cp39-win32.whl)
- [pidng-4.0.9-cp310-cp310-win32.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp310-cp310-win32.whl)
- [pidng-4.0.9-cp311-cp311-win32.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp311-cp311-win32.whl)
- [pidng-4.0.9-cp312-cp312-win32.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp312-cp312-win32.whl)
- [pidng-4.0.9-cp313-cp313-win32.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp313-cp313-win32.whl)
- [pidng-4.0.9-cp314-cp314-win32.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp314-cp314-win32.whl)

#### macOS

- [pidng-4.0.9-cp39-cp39-macosx_11_0_arm64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp39-cp39-macosx_11_0_arm64.whl)
- [pidng-4.0.9-cp310-cp310-macosx_11_0_arm64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp310-cp310-macosx_11_0_arm64.whl)
- [pidng-4.0.9-cp311-cp311-macosx_11_0_arm64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp311-cp311-macosx_11_0_arm64.whl)
- [pidng-4.0.9-cp312-cp312-macosx_11_0_arm64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp312-cp312-macosx_11_0_arm64.whl)
- [pidng-4.0.9-cp313-cp313-macosx_11_0_arm64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp313-cp313-macosx_11_0_arm64.whl)
- [pidng-4.0.9-cp314-cp314-macosx_11_0_arm64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp314-cp314-macosx_11_0_arm64.whl)
- [pidng-4.0.9-cp39-cp39-macosx_10_9_x86_64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp39-cp39-macosx_10_9_x86_64.whl)
- [pidng-4.0.9-cp310-cp310-macosx_10_9_x86_64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp310-cp310-macosx_10_9_x86_64.whl)
- [pidng-4.0.9-cp311-cp311-macosx_10_9_x86_64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp311-cp311-macosx_10_9_x86_64.whl)
- [pidng-4.0.9-cp312-cp312-macosx_10_13_x86_64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp312-cp312-macosx_10_13_x86_64.whl)
- [pidng-4.0.9-cp313-cp313-macosx_10_13_x86_64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp313-cp313-macosx_10_13_x86_64.whl)
- [pidng-4.0.9-cp314-cp314-macosx_10_15_x86_64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp314-cp314-macosx_10_15_x86_64.whl)

#### Linux

- [pidng-4.0.9-cp39-cp39-manylinux1_x86_64.manylinux_2_28_x86_64.manylinux_2_5_x86_64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp39-cp39-manylinux1_x86_64.manylinux_2_28_x86_64.manylinux_2_5_x86_64.whl)
- [pidng-4.0.9-cp310-cp310-manylinux1_x86_64.manylinux_2_28_x86_64.manylinux_2_5_x86_64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp310-cp310-manylinux1_x86_64.manylinux_2_28_x86_64.manylinux_2_5_x86_64.whl)
- [pidng-4.0.9-cp311-cp311-manylinux1_x86_64.manylinux_2_28_x86_64.manylinux_2_5_x86_64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp311-cp311-manylinux1_x86_64.manylinux_2_28_x86_64.manylinux_2_5_x86_64.whl)
- [pidng-4.0.9-cp312-cp312-manylinux1_x86_64.manylinux_2_28_x86_64.manylinux_2_5_x86_64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp312-cp312-manylinux1_x86_64.manylinux_2_28_x86_64.manylinux_2_5_x86_64.whl)
- [pidng-4.0.9-cp313-cp313-manylinux1_x86_64.manylinux_2_28_x86_64.manylinux_2_5_x86_64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp313-cp313-manylinux1_x86_64.manylinux_2_28_x86_64.manylinux_2_5_x86_64.whl)
- [pidng-4.0.9-cp314-cp314-manylinux1_x86_64.manylinux_2_28_x86_64.manylinux_2_5_x86_64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp314-cp314-manylinux1_x86_64.manylinux_2_28_x86_64.manylinux_2_5_x86_64.whl)
- [pidng-4.0.9-cp39-cp39-manylinux2014_aarch64.manylinux_2_17_aarch64.manylinux_2_28_aarch64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp39-cp39-manylinux2014_aarch64.manylinux_2_17_aarch64.manylinux_2_28_aarch64.whl)
- [pidng-4.0.9-cp310-cp310-manylinux2014_aarch64.manylinux_2_17_aarch64.manylinux_2_28_aarch64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp310-cp310-manylinux2014_aarch64.manylinux_2_17_aarch64.manylinux_2_28_aarch64.whl)
- [pidng-4.0.9-cp311-cp311-manylinux2014_aarch64.manylinux_2_17_aarch64.manylinux_2_28_aarch64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp311-cp311-manylinux2014_aarch64.manylinux_2_17_aarch64.manylinux_2_28_aarch64.whl)
- [pidng-4.0.9-cp312-cp312-manylinux2014_aarch64.manylinux_2_17_aarch64.manylinux_2_28_aarch64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp312-cp312-manylinux2014_aarch64.manylinux_2_17_aarch64.manylinux_2_28_aarch64.whl)
- [pidng-4.0.9-cp313-cp313-manylinux2014_aarch64.manylinux_2_17_aarch64.manylinux_2_28_aarch64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp313-cp313-manylinux2014_aarch64.manylinux_2_17_aarch64.manylinux_2_28_aarch64.whl)
- [pidng-4.0.9-cp314-cp314-manylinux2014_aarch64.manylinux_2_17_aarch64.manylinux_2_28_aarch64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp314-cp314-manylinux2014_aarch64.manylinux_2_17_aarch64.manylinux_2_28_aarch64.whl)
- [pidng-4.0.9-cp39-cp39-musllinux_1_2_x86_64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp39-cp39-musllinux_1_2_x86_64.whl)
- [pidng-4.0.9-cp310-cp310-musllinux_1_2_x86_64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp310-cp310-musllinux_1_2_x86_64.whl)
- [pidng-4.0.9-cp311-cp311-musllinux_1_2_x86_64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp311-cp311-musllinux_1_2_x86_64.whl)
- [pidng-4.0.9-cp312-cp312-musllinux_1_2_x86_64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp312-cp312-musllinux_1_2_x86_64.whl)
- [pidng-4.0.9-cp313-cp313-musllinux_1_2_x86_64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp313-cp313-musllinux_1_2_x86_64.whl)
- [pidng-4.0.9-cp314-cp314-musllinux_1_2_x86_64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp314-cp314-musllinux_1_2_x86_64.whl)
- [pidng-4.0.9-cp39-cp39-musllinux_1_2_aarch64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp39-cp39-musllinux_1_2_aarch64.whl)
- [pidng-4.0.9-cp310-cp310-musllinux_1_2_aarch64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp310-cp310-musllinux_1_2_aarch64.whl)
- [pidng-4.0.9-cp311-cp311-musllinux_1_2_aarch64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp311-cp311-musllinux_1_2_aarch64.whl)
- [pidng-4.0.9-cp312-cp312-musllinux_1_2_aarch64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp312-cp312-musllinux_1_2_aarch64.whl)
- [pidng-4.0.9-cp313-cp313-musllinux_1_2_aarch64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp313-cp313-musllinux_1_2_aarch64.whl)
- [pidng-4.0.9-cp314-cp314-musllinux_1_2_aarch64.whl](https://github.com/Ljzd-PRO/PiDNG/releases/download/v4.0.9/pidng-4.0.9-cp314-cp314-musllinux_1_2_aarch64.whl)

***

Credits
------------
Source referenced from:

CanPi ( Jack ) | [color-matrices](https://www.raspberrypi.org/forums/viewtopic.php?f=43&t=278828)

Waveform80 | [picamera](https://github.com/waveform80/picamera)

Krontech | [chronos-utils](https://github.com/krontech/chronos-utils)

Andrew Baldwin | [MLVRawViewer](https://bitbucket.org/baldand/mlrawviewer)

