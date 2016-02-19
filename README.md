# Automatic parenthesis matching patch for the acme text editor.

## File

acme/patch-acme-paren

## Description

This is a patch for plan9port's acme which implements automatic
parenthesis matching. The characters that are matched, are the normal ones
already supported by acme's paren-matching. 

Currently, parenthesis matching is hardcoded, and can not be turned off, though
it should not be difficult to implement a commandline option yourself.


## Notes

- With acme's default colours, the highlighting is hardly noticable. You may
  need to change the (highlighting) colours in **acme.c**.  For example, make
  the default yellow for highlighting a bit darker.

- The modified file is **text.c**, see the patch.


Modified from and tested with: plan9port version 20140306.


## Install

- Move/copy the patchfile to

     ../src/cmd/

- cd to
    ../src/cmd/acme/

- apply the patch

    $ patch -Np1 < ../patchfile 2>&1 | tee log

- if **tee(1)** is not available, or you don't want to use it:

    $ patch -Np1 < ../patchfile 2>&1


## See also:
[https://github.com/9fans/plan9port](https://github.com/9fans/plan9port)

