## My personal latex files for my blog.

I use latex to generate pdf and inkscape to generate svg files.

Normally , I would use dvisvgm but it have a Ghostscript not found bug.

This is my workflow(macos)

```bash
# 1. install latex
# 2. install inkscape
# 3. link inkscape bin
ln -s /Applications/Inkscape.app/Contents/MacOS/inkscape \
  /usr/local/bin/inkscape
# 4. to pdf
latex file.tex
# 5. to svg
inkscape -lD file.pdf --export-type=svg

# -l strip all inkscape related info to reduce file dize
# -D shrink to content not the whole page


# more over, you can use svgo, and reduce ~40% file size
```
