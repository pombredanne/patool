title: portable archive file manager
description: patool is a portable archive file manager
slug: index
---
Introduction
-------------
[![XKCD Tar comic](http://imgs.xkcd.com/comics/tar.png)](http://xkcd.com/1168/)

I could never remember the correct options for all those different compression
programs. Tar, unzip, gzip - you name it and I forgot it.
Patool remembers all those options for me now so I don't have to.

Description
------------
Various archive types can be  created,  extracted,  tested, listed,
compared, searched  and
repacked with patool. The advantage of patool is its simplicity in
handling archive files without having to remember a  myriad  of
programs and options.

The  archive format is determined by the file(1) program and as
a fallback by the archive file extension.

patool supports 7z (.7z, .cb7), ACE (.ace, .cba), ADF (.adf), ALZIP (.alz),
APE  (.ape), AR (.a), ARC (.arc), ARJ (.arj), BZIP2 (.bz2),
CAB (.cab), COMPRESS (.Z), CPIO (.cpio), DEB  (.deb),  DMS  (.dms),
FLAC  (.flac), GZIP (.gz), ISO (.iso), LRZIP (.lrz), LZH (.lha, .lzh),
LZIP (.lz), LZMA (.lzma), LZOP (.lzo), RPM (.rpm), RAR (.rar, .cbr),
RZIP (.rz),  SHN  (.shn), TAR (.tar, .cbt), XZ (.xz),
ZIP (.zip, .jar, .cbz) and ZOO (.zoo) archive formats.
It relies on helper applications to handle those archive formats
(for example bzip2 for BZIP2 archives).

The  archive  formats  TAR, ZIP, BZIP2 and
GZIP are supported natively and  do  not  require  helper
applications to be installed.

Installation
-------------
The easy way with pip:

```bash
sudo pip install patool
```

And on Windows:

```bash
c:\python2.7\scripts\pip install patool
```

Or after downloading the patool .whl file:

```bash
c:\python2.7\scripts\pip install patool-1.9-py2.py3-none-any.whl
```

For Python 2.x you'll need at least Python 2.7, for Python 3.x at least Python 3.3.

If you install from source read the
[installation instructions](https://github.com/wummel/patool/blob/master/doc/install.txt).

Running
--------
After installation there should be a ```/usr/bin/patool``` binary under Unix
systems, under Windows should exist a file ```c:\python2.7\scripts\patool```.

Use ```patool``` to run for Linux or OSX systems,  on Windows use
```c:\python2.7\python2.7.exe c:\python2.7\scripts\patool```.

See the following chapter for usage examples.

Examples
---------

```bash
# extract two archives
patool extract archive.zip otherarchive.rar

# test if archive is intact
patool test --verbose dist.tar.gz

# list files inside an archive
patool list package.deb

# create a new archive
patool create --verbose myfiles.zip file1.txt dir/

# list differences between two archive contents
patool diff release1.0.tar.gz release2.0.zip

# search archive contents
patool search "def urlopen" python-3.3.tar.gz

# compress the archive in a different format
patool repack linux-2.6.33.tar.gz linux-2.6.33.tar.bz2
```

Donate
-------
If you like patool, consider a donation to support it. Thanks!

<form action="https://www.paypal.com/cgi-bin/webscr" method="post">
<input type="hidden" name="cmd" value="_s-xclick">
<input type="hidden" name="hosted_button_id" value="Q6MN5AS8PMCVY">
<input type="image" src="./images/paypal-donate-button.png" border="0" name="submit" alt="PayPal donation">
</form>

<a href="http://flattr.com/thing/1208862/a-portable-archive-file-manager" target="_blank">
<img src="http://api.flattr.com/button/flattr-badge-large.png" alt="Flattr this" title="Flattr this" border="0" /></a>
