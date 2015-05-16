This script converts in a [lossless manner a DVD into a MKV file](http://aperiodic.net/phil/archives/Geekery/lossless-dvd-to-mkv.html).  To use it just run

    ./dvd2mkv

Some environment variables can override its auto-discovery:

 * **`DVD`:** by default it will use the first DVD drive it finds
 * **`TRACK`:** occasionally 'longest track' is incorrect

For example, you can use:

    env TRACK=2 DVD=/dev/dvd3 ./dvd2mkv

## Issues

 * put more tracks into the same mkv
 * add chapters
 * `SIZE` is not accurate
 * OCR VobSub and add a second set of subtitles that are pure text

# Preflight

## Debian

You need will need a Debian Jessie system with the following apt-get repositories:
 * [Debian Multimedia](http://www.deb-multimedia.org/)

Now run:

    sudo apt-get install -yy --no-install-recommends lsdvd libdvdcss2 xmlstarlet transcode pv mkvtoolnix fuseiso9660 subtitleripper

### Wheezy

If you are still on Wheezy, then you will need the following apt-get repositories:
 * Debian Backports
 * [Debian Multimedia](http://www.deb-multimedia.org/)
 * [MKVToolNix](https://www.bunkus.org/videotools/mkvtoolnix/downloads.html#debian)

Once plumbed in, install the dependencies with (`mkvtoolnix` needs to be from bunkus):

    sudo apt-get install -yy --no-install-recommends -t wheezy-backports lsdvd libdvdcss2 xmlstarlet transcode pv mkvtoolnix fuseiso9660 subtitleripper
