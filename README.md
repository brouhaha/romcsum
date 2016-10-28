# romcsum - Compute checksum and CRC32 of ROM images

Copyright 2016 Eric Smith <spacewar@gmail.com>

romcsum development is hosted at the
[romcsum Github repository](https://github.com/brouhaha/romcsum/).

## Introduction

Two different integrity checks are commonly used for ROM
(masked, EPROM, EEPROM, flash) memory images.

* Nearly all EPROM programmers use a simple checksum of either 16 or
  32 bits, with carries ignored.  This is actually a terrible
  integrity check, because it cannot detect transposed byte, or
  dropped zero bytes.  Its use is not recommended for any reason other
  than that EPROM programmers already do it.

* Some software, including MAME, uses a CRC32, which is far better at
  error detection.

romcsum is a Python program that will compute the simple checksum,
CRC32, or both for a list of ROM images supplied on the command line.
By default romcsum reads raw binary image files, but the '--hex'
command line option will cause it to read Intel Hex format instead.

## License information:

This program is free software: you can redistribute it and/or modify
it under the terms of version 3 of the GNU General Public License
as published by the Free Software Foundation.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
