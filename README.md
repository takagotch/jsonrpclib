### jsonrpclib
---
https://github.com/joshmarshall/jsonrpclib/

```py
// tests.py
try:
  import json
except ImportError:
  import simplejson as json
import os
import socket
import sys
import tempfile
from threading import Thread

if sys.version_info < (2, 7):
  import unittest2 as unittest
else:
  import unittest

from jsonrpclib import Server, MultiCall, history, ProtocolError
from jsonrpclib import jsonrpc
from jsonrpclib.SimpleJSONRPCServer import SimpleJSONRPCServer
from jsonrpclib.SimpleJSONRPCServer import SimpleJSONRPCRequestHandler

def get_port(family=socket.AF_INET):
  sock = socket.socket(family, socket.SOCK_STREAM)
  sock.bind(("localhost", 0))
  return sock.getsockname()[1]

class TestCompatibility(unittest.TestCase):

  client = None
  port = None
  server = None
  
  def setUp(self):
    self.port = get_port()
    self.server = server_set_up(addr_('', self.port))
    self.client = Server('http://localhost:%d' % self.port)

  def test_positional(self):
  
  def test_named(self):




```

```
```

```
```
