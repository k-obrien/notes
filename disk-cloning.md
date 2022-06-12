# Disk Cloning

**Note**: _Some of these steps are specific to FreeBSD in general, and to TrueNAS in particular._

## Create a forensic disk image

- _The base system must be used to allow access to device nodes._
- _Perform all operations in a screen session so as not to interrupt long-running operations._
- _Ensure the `ddrescue` binary exists in the working directory. It can be installed inside a jail using `pkg install ddrescue` and copied out to the base system from `/usr/local/bin/ddrescue`_

Attach the disk and identify its device node using the output of `gpart show`

Perform an initial single pass over the disc with ddrescue so as not to stress a failing drive more than necessary with, e.g., `ddrescue -n /dev/sd0 clone.img clone.txt`

Perform a second pass if necessary, retrying three times on errors, with `ddrescue -r3 /dev/sd0 clone.img clone.txt`

## Access a disk image using the loop device

Use `mdconfig clone.img` to attach the image and `mdconfig -d -u 0` to detach, assuming the assigned device unit was 0. The assigned unit can be determined with `mdconfig -lf clone.img`.

## Clone a filesystem with rsync

Clone a filesystem with optimisations which generally aren't needed when transferring files locally,  such as disabling compression and file comparison, using `rsync -ahW --no-perms --compress-level=0 --info=progress2 src/ dest/`. Note the trailing slashes.
