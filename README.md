# NeewerLite-Python
NeewerLite-Python is an un-official cross-platform Neewer LED light control app - written in Python, originally based off of the NeewerLite macOS Swift project by @keefo (Xu Lian). NeewerLite-Python can be used on Windows, Mac and Linux, and can be used as a GUI (the normal way to use it), as a CLI (control one light from the command line), or as an HTTP server (keep persistant connections to lights active, but unlike the GUI, allow communication from remote devices like phones and Streamdecks to control single or multiple lights from a web browser!)

Read the manual here: https://github.com/taburineagle/NeewerLite-Python/wiki

## macOS Infinity lights: hardware MAC override
Some Infinity-protocol lights on macOS report a BLE GUID instead of a hardware MAC. If you see errors about a missing hardware MAC, you can add a persistent override file:

1. Copy `hardwareMACs.prefs.example` to `light_prefs/hardwareMACs.prefs`
2. Add one mapping per line in the format `GUID=AA:BB:CC:DD:EE:FF`
3. Restart NeewerLite-Python (GUI/HTTP/CLI) to load the overrides

Note: I observed this on two TL60 lights where one advertised as `TL60 RGB` and required a hardware MAC override on macOS, while the other advertised as `NW-20240061&92A10500` and worked without an override.

**Added default settings for these lights (not all of these lights are Bluetooth controllable, so... your mileage may very):** GL1, NL140 SNL1320, SNL1920, SNL480, SNL530, **SNL660**, SNL960, SRP16, SRP18, WRP18, ZRP16, BH30S, CB60, CL124, RGB C80, RGB CB60, RGB1000, RGB1200, RGB140, RGB168, RGB176 A1, RGB512, RGB800, SL-90, RGB1, **RGB176**, RGB18, RGB190, RGB450, **RGB480**, RGB530 PRO, RGB530, RGB650, **RGB660 PRO**, RGB660, RGB960, RGB-P200, RGB-P280, SL-70, **SL-80**, ZK-RY

**Fully tested Neewer lights (in bold above) so far:** SL-80, SNL-660, RGB660 PRO, 480 RGB, RGB176
 
![0 12 Windows](https://user-images.githubusercontent.com/18430526/174457747-132d69ed-5130-49c3-b0f6-9e45e3013081.png)
