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