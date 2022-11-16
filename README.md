### My Build of slock:

### Applied Patches
- [DPMS](https://tools.suckless.org/slock/patches/dpms/): This patch interacts with the Display Power Management Signaling and automatically turns off the monitor after a configurable time. The monitor is reactivated by a keystroke or moving the mouse.

- [control-clear](https://tools.suckless.org/slock/patches/control-clear/): Adds an additional configuration parameter, controlkeyclear. When set to 1, slock will no longer change to the failure color if a control key is pressed while the buffer is empty. This is useful if, for example, you wake your monitor up by pressing a control key and don't want to spoil the detection of failed unlocking attempts.

### Requirements/Dependencies
In order to build slock you need the Xlib header files.

- libxcb
- Xlib-libxcb
- xcb-res
- libxinerama
- libx11

### Configuration and installation
Edit config.mk to match your local setup (slock is installed into the /usr/local namespace by default).

The configuration of slock is done copying [config.def.h](config.def.h) to `config.h`, editing it and then (re)compiling the source code.
