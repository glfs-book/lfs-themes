# lfs-themes

A collection of Linux From Scratch themes (CSS files) to be used with the `*LFS`
books.

This repository is intended for the SLFS and GLFS books made by the GLFS
development team and its contributors, but can also be used for LFS, MLFS, and
BLFS.

## In use with GLFS/SLFS

For Gaming or Supplemental LFS, when rendering the books, you can run the
following:
```Bash
make <options> \
THEME_PATH=/path/to/lfs-themes/themes \
THEME=<theme>
```

For example, assuming you have SLFS and lfs-themes in `/sources`, you could
build SLFS using the 'whitepink' theme like so:
```Bash
cd /sources/slfs
make REV=sysv THEME_PATH=../lfs-themes/themes THEME=whitepink
```

## In use with LFS/MLFS/BLFS

The LFS, MLFS, and BLFS Makefiles do not support the `THEME` or `THEME_PATH`
variables, so the default theme must be overwritten. The theme may be
overwritten at build or install time.

### Build Time Overwriting
To overwrite the default theme at build time:
```Bash
cp -vf /path/to/lfs-themes/themes/<theme>.lfs.css /path/to/book/sources/stylesheets/lfs-xsl/lfs.css
```

Replace `<theme>` with the theme you wish to use. Then just build the book as usual.

### Install Time Overwriting
Alternatively, to overwrite the default theme at install time:
```Bash
cp -vf /path/to/lfs-themes/themes/<theme>.lfs.css /path/to/rendered/book/stylesheets/lfs.css
```

Replace `<theme>` with the theme you wish to use.

## Contributing
Fork this repository and `git checkout` to a new branch. Copy an existing theme
and edit it to your heart's content. Once you've completed your masterpiece,
push to your fork, then submit a pull request.
