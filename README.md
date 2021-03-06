Cbump is a POSIX C implementation of Open_Bump/Bump! with improvements.
The original Bump! is web based implementation and the Open_Bump is
Python, both can't run on Android.

So, you can bump any kernel or recovery directly on your device.

The full cmdline interface:

```
shell@g2:/ $ cbump
usage: cbump [-f|--flash] [-a|--avexado] [stdin] [stdin]

[stdin] : Bump file if not bumped, output is writed with 'c' prefix.
[-f|--flash] : Check if file is bumped and flash.
[-a|--avexado] : Check if file is bumped, bump file if not and flash.
Cbump indentify partition by file name, (e.g, If you use -f with a recovery.img file, cbump flash as recovery)
```

The flash function uses MSM identifier to detect partition block, Tested only on LG G2, Probably works too with LG G3 and others LG devices powered by Qualcomm.

References:

* https://android.googlesource.com/platform/system/core
* https://github.com/djrbliss/loki
* https://github.com/CyboLabs/Open_Bump
