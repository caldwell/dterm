dtermd
======

dtermd is a serial to telnet bridge. When you start the daemon it connects to a
serial port and listens on a socket (localhost:10000). Then you `telnet
localhost 10000` to start a serial session. The nice thing is that it supports
multiple telnet clients per serial port--any client can type and the data coming
from the serial port gets copied out to each client. This lets every connected
client see what is going on and optionally control it, which opens the door to
many possible uses:

  * Sharing a single hardware device amongst many developers.
  * Pair programming for embedded developers.
  * Demos.
  * etc.

Usage
-----

    dtermd [<tty> [<baud>]]

`<tty>` is your serial device. Typically `/dev/USB0` on Linux or
`/dev/cu.usbserial` on Mac OS X.

`<baud>` is the baud rate. It defaults to 115200.

License
-------

Copyright © 2006-2015 David Caldwell <david@porkrind.org>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
