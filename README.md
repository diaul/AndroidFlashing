# AndroidFlashing
Commands usefull fo flash Android Pixel Phones

## Downloads
Android Pixel Images https://developers.google.com/android/images 
Android Platform Tools (e.g. adb, fastboot) https://developer.android.com/studio/releases/platform-tools 

## Commands
```
./fastboot --slot=all flash bootloader ../raven-sq3a.220705.004/bootloader-raven-slider-1.2-8318357.img 
./fastboot reboot bootloader
./fastboot --slot=all flash radio ../raven-sq3a.220705.004/radio-raven-g5123b-100840-220505-b-8544885.img 
./fastboot reboot bootloader
```

