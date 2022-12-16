st - simple terminal
--------------------
st is a simple terminal emulator for X which sucks less.

This is my Char-custom branch with a few patches from st.suckless.org already applied:
* alpha
* blinking_cursor
* desktopentry
* glyph-wide-support
* hidecursor


TODO
----
* Create a new patch to paste from clipboard with Shift+MMB while keeping the current primary selection behavior
* Apply all the scrollback patches from http://st.suckless.org/patches/scrollback/
* Try out the anysize/anygeometry patches to see which can put the content in the middle
    - If both can, use whichever makes the least changes. For now it looks like anysize is probably the winner.
* Try out http://st.suckless.org/patches/ligatures/ plus Ligconsolata as the font (to avoid needing font2)


Requirements
------------
In order to build st you need the Xlib header files.


Installation
------------
Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install


Running st
----------
If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

Credits
-------
Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.

