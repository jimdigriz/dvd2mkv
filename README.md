This script converts in a lossless manner a DVD into a MKV file.  To use it just run

    sh dvd2mkv

It will use the first DVD drive it finds, but you can override this by setting the environment variable `DVD` to point to the source device

The method here was cribbed from http://aperiodic.net/phil/archives/Geekery/lossless-dvd-to-mkv.html

# Preflight

You need will need at least a Debian Wheezy system with the following apt-get repositories:
 * Debian Backports
 * Debian Multimedia - http://www.deb-multimedia.org/
 * MKVToolNix - https://www.bunkus.org/videotools/mkvtoolnix/downloads.html#debian

    sudo apt-get install -yy --no-install-recommends -t wheezy-backports lsdvd libdvdcss2 xmlstarlet transcode pv mkvtoolnix fuseiso9660 subtitleripper

# Issues

 * put more tracks into the same mkv
 * add chapters
 * `SIZE` is not accurate
 * OCR VobSub and add a second set of subtitles that are pure text
