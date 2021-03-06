Docker Ffmpeg Srt Compiler
==========================

Docker Ffmpeg Srt Compiler is a zero-set-up solution to install a fully featured ffmpeg binary on a linux system.
All credit goes to the original author in https://github.com/srwareham/docker-ffmpeg-compiler (browse there for anhanced instructions),
but this fork also adds HayVision libSRT support and a couple naming conventions for my build system.

Running without cloning
-----------------------

This is the original installation method from the forked project. It conveniently creates the ffmpeg binaries in the calling directory.

.. code-block:: bash

    bash -c "$(curl -fsSL https://raw.githubusercontent.com/nebular/docker-build-ffmpeg-srt/master/install.sh)"

Running by cloning
-------------------

To further integrate this project in a bigger one, an alternate installation method is provided

.. code-block:: bash

    git clone https://github.com/nebular/docker-build-ffmpeg-srt
    cd docker-build-ffmpeg-srt
    ./compile.sh

This method does not erase the docker image, and creates the output in $PWD/out/usr/local/bin.

Codecs and Features
===================

Video
-----

- `x264 <https://www.videolan.org/developers/x264.html>`_
- `x265 <http://x265.org/>`_
- `Theora <https://www.theora.org/>`_
- `VP8 <http://www.webmproject.org/>`_ / `VP9 <http://www.webmproject.org/vp9/>`_
- `SRT <https://github.com/Haivision/srt>`_

Audio
-----
- `fdk-aac <https://github.com/mstorsjo/fdk-aac>`_
- `lame (mp3) <http://lame.sourceforge.net/>`_
- `Vorbis <http://www.vorbis.com/>`_
- `Opus <https://www.opus-codec.org/>`_

Other
-----

- `libass <https://github.com/libass/libass>`_
- `freetype <http://www.freetype.org/>`_

Dependencies
============

- A Docker installation is needed.
