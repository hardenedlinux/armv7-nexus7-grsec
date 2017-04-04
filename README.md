Maintainer: Shawn C[a.k.a "citypw"], citypw@gmail.com

Thanks to:

- [PaX/Grsecurity](http://grsecurity.net/)

Copyright (c) TYA infotech ltd http://tya.company/


# [PoC: PaX for Android](https://github.com/hardenedlinux/armv7-nexus7-grsec)

This project is a PoC to proved Android kernel can be protected by PaX/Grsecurity. Most of work has done in May 28 2015.

Testing environment:

flo( Nexus 7 2017)
- [Android NDK 9d](http://dl.google.com/android/ndk/android-ndk-r9b-linux-x86.tar.bz2)
- [Android 4.4](https://dl.google.com/dl/android/aosp/razor-ktu84p-factory-2482a7d5.zip)
- [msm-flo-kit](https://android.googlesource.com/kernel/msm/+/android-msm-flo-3.4-kitkat-mr2)

marlin( Pixel XL)
- [nougat aarch64 toolchain)(https://android.googlesource.com/platform/prebuilts/gcc/linux-x86/aarch64/aarch64-linux-android-4.9/+archive/nougat-release.tar.gz)
- [Android 7.1.1](https://android.googlesource.com/platform/prebuilts/gcc/linux-x86/aarch64/aarch64-linux-android-4.9/+archive/nougat-release.tar.gz)
- [msm-marlin-3.18-nougat](https://android.googlesource.com/kernel/msm/+/android-msm-marlin-3.18-nougat-mr1.3)

Notes: The combination of PXN( inspired by PaX's KERNEXEC), HARDENED_USERCOPY( implemented and ported from PaX/Grsecurity's PAX_USERCOPY partially), RO vdso, DEBUG_RODATA/STRICT_MEMORY_RWX( it originally implemented by PaX's KERNEXEC) is unlikely to defeat highly customized exploitation( even some exploit vectors, which old dudes forgot already and new dudes never know) but it's strong enough to defeat those easy-to-write exploits uased by malwares, which might cause massive affection.


Write-up:
 * [Linux kernel mitigation checklist](https://hardenedlinux.github.io/system-security/2016/12/13/kernel_mitigation_checklist.html)
 * [How can we "hardened" an Android eco-system without Google?](http://citypw.blogspot.ca/2016/08/how-can-we-hardened-android-eco-system.html)
 * [PaX/Grsecurity for Nexus 7 2013](https://hardenedlinux.github.io/system-security/2015/05/11/Grsecurity-for-Nexus-7-2013.html)
