# st - simple terminal

Build of st by [Rafael Cavalcanti](https://rafaelc.org/dev).

st is a simple terminal emulator for X which sucks less.

## Third party patches

- anysize
- boxdraw
- externalpipe
- font2
- glyph-wide-support-boxdraw patch
- newterm
- vim patch: historyVanilla, patch_scrollback and patch_column. This fixes horizontal resizing and brings scrollback.
- w3m - alpha seems incompatible with this.
- workingdir
- xresources

## My own patches

- Add desktop file. This fixes missing icon on docks.
- Complement to vim patch: scroll with mouse.
- Allow custom cursor color.

## Requirements

In order to build st you need the Xlib header files.

## Installation

Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install

## Running st

If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

## Credits

Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.

