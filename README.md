# AndroidFlashing
Commands usefull fo flash Android Pixel Phones

## Downloads
- Android Pixel Images https://developers.google.com/android/images 
- Android Platform Tools (e.g. adb, fastboot) https://developer.android.com/studio/releases/platform-tools 

## Commands

Flashing bootloader
```
./fastboot --slot=all flash bootloader ../raven-sq3a.220705.004/bootloader-raven-slider-1.2-8318357.img 
./fastboot reboot bootloader
```

Flashing radio
```
./fastboot --slot=all flash radio ../raven-sq3a.220705.004/radio-raven-g5123b-100840-220505-b-8544885.img 
./fastboot reboot bootloader
```

Flashing system image
```
./fastboot --skip-reboot --slot=all update ../raven-sq3a.220705.004/image-raven-sq3a.220705.004.zip
```

If you get the error:

```
Resizing 'vendor_b'                                FAILED (remote: 'Not enough space to resize partition')
```

Trying this solved my problem (don't know why it works):

```
./fastboot --skip-reboot update ../raven-sq3a.220705.004/image-raven-sq3a.220705.004.zip
./fastboot --skip-reboot --slot=other update ../raven-sq3a.220705.004/image-raven-sq3a.220705.004.zip  
```

