# 2011_1007_RT5390_RT5392_Linux_STA_V2.5.0.3_DPO_v2

Some source code from mediatek

FIX FOR RALINK WLAN DRIVER:

1. download archive
2. extract content
3. cd 2011_1007_RT5390_RT5392_Linux_STA_V2.5.0.3_DPO
4. copy file patch in 2011_1007_RT5390_RT5392_Linux_STA_V2.5.0.3_DPO
5. patch -p1 <rt5592sta_fix_64bit_3.8.patch (if asks for directory point it to pci_main_dev.c)
6. make sure /os/linux/config.mk reads HAS_NATIVE_WPA_SUPPLICANT_SUPPORT=y
7. make
8. sudo make install
9. modprobe rt5390sta 

You may need to disable some other drivers in /etc/modprobe.d/blacklist.conf 

    ## Blacklist conflicting kernel modules
    blacklist rt2800pci
    blacklist rt2800lib
    blacklist rt2x00usb
    blacklist rt2x00pci
    blacklist rt2x00lib
    blacklist rt2860sta
    blacklist rt3090sta

