# lfs-themes

A collection of Linux From Scratch themes (CSS files) to be used with the
`*LFS*` books.

This repository is namely meant for the LFS books made by the GLFS development
team and its contributors, but can be used for the books made by the LFS and
BLFS development teams (LFS, MLFS, and BLFS).

## In use with GLFS/SLFS

For Gaming or Supplemental LFS, when rendering the books, you can run the
following:
```Bash
make <options> \
THEME_PATH=/path/to/lfs-themes/themes \
THEME=<theme>
```

`<options>` corrospond to specific options used by the `Makefile` of each book,
while `<theme>` should be `themes/<theme>.lfs.css`. For example, if you want to
use the GLFS dark theme (`themes/glfs-dark.lfs.css`), set `*THEME` to
`glfs-dark`.

## Manual use

This is used for already rendered LFS books, and is the only way to get themes
working with books made by the LFS and BLFS development teams. This skips the
need to render anything, but requires to be redone everytime a new book version
is on the system.

This also requires the book to be on the system, though may be possible to
replace the CSS being used when viewed online.

Generally, this is how it should be done:
```Bash
cp -v /path/to/lfs-themes/themes/<theme>.lfs.css /path/to/book/stylesheets/lfs.css
```

Replace `<theme>` with the theme you wish to use.

## Contributing
Fork this repository and check out to a new branch. Copy an existing theme[^1]
and edit it to your heart's content. Once you've completed your masterpiece,
push to your fork, then submit a pull request.

[^1]: A template theme will be added in the future.
