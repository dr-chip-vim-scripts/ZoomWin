About ZoomWin
=============

Note: version 23 or later of ZoomWin requires vim 7.2 or later

Usage:

**Press <c-w>o**: the current window zooms into a full screen

**Press <c-w>o again**: the previous set of windows is restored

Features:

The idea is to make it easy to zoom into and out of a window.
ZoomWin supports normal windows, and it now also supports scratch-windows, no-name windows, and modified-buffer windows.

* ZoomWin is a 7.2 plugin (as of v23)

* Files are made hidden during zoom-in and restored upon zoom-out

* All windows' file contents will be restored during zoomouts.

* ZoomWin will clean up any temporary files it generates upon exit.

* Session files are guaranteed to be unique to each vim session, so multiple vims can use zoom-in/out without interfering with one another

A later version may be available at http://www.drchip.org/astronaut/vim/index.html#ZOOMWIN .

When zooming in, ZoomWin's window is full sized, with no loss of screen space to status lines for other windows, unlike vimscript#1280 (ToggleOnly), for those vims compiled with the +mksession feature.  For those vims without that feature, v21 ZoomWin now supports partial-zoom-in (leaves a status line behind for each window).

History:

Ron Aaron came up with the original ZoomWin and gave permission to have it posted.


About this repository
=====================


This is an unofficial repository to keep updated the ZoomWin vim plugin.

The idea behind this is to unite efforts of all the people that have been doing (almost) the same in different forks:

* keep ZoomWin updated, since Dr. Chip does not have a github account.
* use a github url for `vundle <https://github.com/gmarik/vundle>`_
* add a ``.gitignore`` file to avoid the tags file get indexed.

This initiative was started here:
https://github.com/ivanalejandro0/ZoomWin/issues/1

For the original source go to:
http://drchip.org/astronaut/vim/index.html#ZOOMWIN

Vim.org script page:
http://www.vim.org/scripts/script.php?script_id=508


Instructions to collaborate
===========================

If you want to help keeping this (or other Dr. Chip's plugin) you'll need to:

#. extract the latest plugin.vba.gz file.
#. update the files in the repo
#. update the version in the readme

Extract the vba file
--------------------

::

    mkdir zoomwin && cd zoomwin
    wget http://drchip.org/astronaut/vim/vbafiles/ZoomWin.vba.gz
    vim ZoomWin.vba.gz
        :UseVimball .
        :q
    rm ZoomWin.vba.gz .VimballRecord

Thanks to: http://stackoverflow.com/a/3770585/687989


Update the readme
-----------------

Pick the update line found in http://drchip.org/astronaut/vim/index.html#ZOOMWIN under the download link.

For instance: "Updated Nov 09, 2013 (v25j)"

And add it to the 'History' section of this README.

Note: VERSION = 25j


Update the files in the repo
----------------------------

::

    cp zoomwin.drchip/* -R ZoomWin/
    cd ZoomWin/
    git checkout -b update-to-VERSION
    git add .
    git commit -m "Update ZoomWin to version VERSION."
    git push origin update-to-VERSION

After that, is desirable to wait until someone merge your pull request instead of merging it yourself.

Note:

If you are part of ``dr-chip-vim-scripts`` org, then ``origin`` should be ``git@github.com:dr-chip-vim-scripts/ZoomWin.git``

If you want to collaborate with the latest version and you haven't push access, then ``origin`` should be the url of your fork.


History
=======

* Updated Mar 09, 2014 (v25m)
* Updated Feb 19, 2014 (v25l)
* Updated Nov 09, 2013 (v25j)
* November 24, 2013. Start ``dr-chip-vim-scripts`` org.

For more information, in vim, use ``:h zoomwin-history``.

Or read it online in Dr. Chip's website: http://drchip.org/astronaut/vim/doc/ZoomWin.txt.html
