Welcome to SoCo
===============

SoCo (Sonos Controller) lets you control your [Sonos](http://www.sonos.com/) speakers from Python or the commandline.

Python example
--------------

When using Python, you need the [soco](https://pypi.python.org/pypi/soco) package (see [GitHub project](https://github.com/SoCo/SoCo)).

```` python

# Import soco and get a SoCo instance
import soco
device = soco.discovery.any_soco()

# Get all albums from the music library that contains the word "Black"
# and add them to the queue
albums = device.music_library.get_albums(search_term='Black')
for album in albums:
	print('Added:', album.title)
device.add_to_queue(album)

# Dial up the volume (just a bit) and play
device.volume += 10
device.play()

````

Commandline example
-------------------

For the commandline interface you need the socos package (see [GitHub project](https://github.com/SoCo/socos)).

````

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
