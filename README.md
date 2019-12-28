# Py3tftp

otftpd is an asynchronous [TFTP][1] server written in Python 3.5 compatible with the Oberon sources

This project is a fork of  [https://github.com/sirMackk/py3tftp][2] version 1.2.1
### Installation

```
git clone https://github.com/pedrudehuere/otftpd.git
pip install otftpd
```

### Usage

Invoking pyt3tftp will start a server that will interact with the current working directory - it will read and write files from it so don't run it in a place with sensitive files!

TFTP has no security features, except for its simplicity:
- It won't overwrite files.
- Won't create non-existant directories.
- Cannot write outside of the directory it's running from.

```
usage: otftp [-h] [--host HOST] [-p PORT] [--ack-timeout ACK_TIMEOUT]
             [--conn-timeout TIMEOUT] [-l FILE_LOG] [-v] [--version]
             [--files-dir FILES_DIR]

optional arguments:
  -h, --help            show this help message and exit
  --host HOST           IP of the interface the server will listen on.
                        Default: 0.0.0.0
  -p PORT, --port PORT  Port the server will listen on. Default: 69 (TFTP
                        standard port)
  --ack-timeout ACK_TIMEOUT
                        Timeout for each ACK of the lock-step. Default: 0.5.
  --conn-timeout TIMEOUT
                        Timeout before the server gives up on a transfer and
                        closes the connection. Default: 3.
  -l FILE_LOG, --file-log FILE_LOG
                        Append output to log file.
  -v, --verbose         Enable debug-level logging.
  --version
  --files-dir FILES_DIR
                        Directory where files are read from
```

#### LICENSE

The MIT License (MIT)

Copyright (c) 2016-2018 sirMackk

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.


[1]: https://en.wikipedia.org/wiki/Trivial_File_Transfer_Protocol
[2]: https://github.com/sirMackk/py3tftp
