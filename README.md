# st - simple terminal

Build of st by [Rafael Cavalcanti](https://rafaelc.org/dev), 2021-2024. st is a simple terminal emulator for X which sucks less.

_Notice: To cleanly integrate updates from upstream, this branch might be rebased._

## Third party patches

- alpha
- anysize
- boxdraw
- externalpipe
- "glyph wide support"
- netwmicon
- newterm
- vim patch: historyVanilla, patch_scrollback and patch_column. This fixes horizontal resizing and brings scrollback.
- workingdir
- "xresources with reload signal"

## My own patches

- Add desktop file. This fixes missing icon on docks.
- Complement to vim patch: scroll with mouse.

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

