# st - simple terminal (Command_maker's version)

st is a simple terminal emulator for X which suck less.

## Requirements

In order to build st you need the Xlib header files.
This repository contains a modified version of st which need the `imlib2` library.

## Applied patches

This version of st contains multiple patches applied thanks to [st-flexipatch](https://github.com/bakkeby/st-flexipatch) :
- bold is not bright (don't change the font color when using bold font)
- boxdraw (clean boxes draw and other geometric shapes)
- columns (allow resize without cutting text)
- copyurl (copy urls when clicking)
- delkey (send delete keycode)
- drag and drop (allow to drag and drop files and insert its path)
- font2 (allow multiple font size)
- ligatures (enable ligatures)
- reflow (buffer, history and scrollback patch)
- sixel (image rendering, requires `imlib2`)
- undercurl (allow special underlines)
- wide glyphs patch (prevent icons from nerd fonts to be cropped)

## Installation

Edit `config.mk` to match your local setup (st is installed into /usr/local namespace by default).

Afterwards enter the following command to build and install st (if necessary as root):

```
make clean install
```

## Running st

If you did not install st with `make clean install`, you must compile the st terminfo entry with the following command :

```
tic -sx st.info
```

See the man page for additional details.

## Credits

Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code
