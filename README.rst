DogPetter
=========

|license|

Pet a watchdog to keep it running.

DogPetter is a simple program, with a simple goal: to tend to the Linux
kernel's watchdog, keeping it awake so the system doesn't reboot. If for some
reason the system hangs, and DogPetter stops tending to the watchdog, the Linux
watchdog will do its job and reboot.


Usage
-----

Just run DogPetter directly at the command-line, as root::

  # dogpetter

The program will daemonize to the background. There, it will open the special
file ``/dev/watchdog`` and keep refreshing it periodically, by writing to it
every few seconds.

For more information on the Linux kernel's watchdog, read the file
`Documentation/watchdog/watchdog-api.txt`_ from the Linux kernel source
documentation.


Contact
-------

DogPetter is developed by Israel G. Lugo <israel.lugo@lugosys.com>. Main
repository for cloning, submitting issues and/or forking is at
https://github.com/israel-lugo/dogpetter


License
-------

Copyright (C) 2017 Israel G. Lugo <israel.lugo@lugosys.com>

DogPetter is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

DogPetter is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with DogPetter.  If not, see <http://www.gnu.org/licenses/>.


.. |license| image:: https://img.shields.io/badge/license-GPLv3+-blue.svg?maxAge=2592000
   :target: LICENSE
.. _`Documentation/watchdog/watchdog-api.txt`: https://www.kernel.org/doc/Documentation/watchdog/watchdog-api.txt
