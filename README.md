# python-pgpdump: a Python library for parsing PGP packets

This is based on the C version published at:
http://www.mew.org/~kazu/proj/pgpdump/

The intent here is not on completeness, as we don't currently decode every
packet type, but on being able to do what people actually have to 95% of the
time. Currently supported things include:

* Signature packets
* Public key packets
* Secret key packets
* Trust, user ID, and user attribute packets
* ASCII-armor decoding and CRC check

A single codebase with dependencies on only the standard python library is
compatible across Python 2.7, Python 3.2+, and PyPy 1.8+.

This version of the library has been slightly modified by Thomas Spycher and adds the following funcdtions:

* generation of SKS compatible hashes
* get the latest timestamp of a change in the key

To install this version use the following command
`pip install git+git://github.com/tspycher/python-pgpdump.git#egg=pgpdump`