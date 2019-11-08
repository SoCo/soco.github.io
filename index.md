Welcome to SoCo
===============

SoCo (Sonos Controller) lets you control your [Sonos](http://www.sonos.com/) speakers from Python or the commandline.

Python example
--------------

When using Python, you need the [soco](https://pypi.python.org/pypi/soco) package (see [GitHub project](https://github.com/SoCo/SoCo)).

```` python

import soco
speakers = soco.discover()

speaker = speakers[0]
speaker.play()

````

Commandline example
-------------------

For the commandline interface you need the socos package (see [GitHub project](https://github.com/SoCo/socos)).

```` bash

$ socos list
(1) 192.168.0.129 Living room
(2) 192.168.0.130 Bedroom

$ socos play 192.168.0.129

```

Discuss
-------

If you want to ask questions or start a discussion, you can find us on [Google Groups](https://groups.google.com/forum/#!forum/python-soco).


Related Projects
----------------

* [Automated Intro Music in the Office](http://scottlobdell.me/2014/02/automated-intro-music-in-the-office-python-opencv-gphoto2-and-boost/)
* [Sonos Control server for the Smarthome.py Project](https://github.com/pfischi/shSonos)
