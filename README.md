# Remote Control extension for LogMeIn Linux host

The `logmein-host` extension snap enables the Remote Control feature.


## Installation
1. Install `logmein-host` from the snap store as described [here](https://lmibinarieslive.blob.core.windows.net/linux/index.html#/linux)

2. Install `logmein-rc-extension` with the following command:

```sudo snap install logmein-rc-extension --classic```

## Known issues
### Ubuntu 18.04+
From Ubuntu 18.04 onwards, the default windowing system for gdm is Wayland instead of xorg. This should be changed to the usual xorg to get the remote control work. Simply edit the `/etc/gdm3/custom.conf` config file and change:
```
#WaylandEnable=false
```
to:

```
WaylandEnable=false
```
then restart your system to apply. For further info read [this](
https://linuxconfig.org/how-to-disable-wayland-and-enable-xorg-display-server-on-ubuntu-18-04-bionic-beaver-linux) external post.
