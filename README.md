
# raspbian-build #

This is woodenshoe-wi's fork of the
https://github.com/puppylinux-woof-CE/woof-CE repo.  Please do not base any
commits off this branch or issue any pull requests here, there are commits in
this branch (this readme) that won't be included upstream.

The raspbian-build branch is based off of puppylinux-woof-CE/woof-CE testing,
and contains all of the commits from my most recent successful Raspbian stretch
based build.  It is probably out of date, and you should consider using
puppylinux-woof-CE/woof-CE instead.

This build does **NOT** create an image file.  The files in the zip file
produced need to be placed on a FAT formatted SD card.

If running a version of Puppy Linux older than Slacko 6.3.0 you will need to
replace the version of debdb2pupdb at /usr/local/petget/debdb2pupdb with the one
from woof-out_x86_arm_raspbian_wheezy/support/ (or whatever is right for your
host arch)

If debdb2pupdb is an old version, 0setup gives the following error.

```
...
Checking that compat-distro pkgs specified in PKGS_SPECS_TABLE actually exist...
FAIL: raspberrypi-bootloader-nokernel
...
```

or if you skip the check in 0setup,  
after running 2createpackages ERROR-2CREATEPACKAGES will contain

```
...
ERROR: 'raspberrypi-bootloader-nokernel' package does not exist.
You will need to find a matching package and place in packages-pet,
or packages-deb_raspbian-wheezy as appropriate.
Do it, then rerun this script and choose to build raspberrypi-bootloader-nokernel.
...
```

