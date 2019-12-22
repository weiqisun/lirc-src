# lirc-src
Source and patch of lirc in raspbian buster

## Compile
```
patch -p0 -i lirc-gpio-ir-0.10.patch
cd lirc-0.10.1
debuild -uc -us -b
```

## Install
```
cd ..
sudo apt install ./liblirc0_0.10.1-5.2_armhf.deb ./liblircclient0_0.10.1-5.2_armhf.deb ./lirc_0.10.1-5.2_armhf.deb
```
Above installation will fail. Update lirc configuration at `/etc/lirc/` and run the following again
```
sudo apt install -y --allow-downgrades ./liblirc0_0.10.1-5.2_armhf.deb ./liblircclient0_0.10.1-5.2_armhf.deb ./lirc_0.10.1-5.2_armhf.deb
```
