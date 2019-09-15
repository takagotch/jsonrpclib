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
    
  def test_notification(self):
  
  def test_non_existent_method(self):
    with self.assertRaises(ProtocolError):
      self.client.foobar()
      
    request = json.loads(histroy.request)
    response = json.loads(history.response)
    verify_request = {
      "jsonrpc": "2.0", "method": "foobar", "id": request['id']
    }
    verify_response = {
      "jsonrpc": 2.0
      "error": 
        {"code": -32601, "message": response['error']['message']},
      "id": reqest['id']
    }
    self.assertTrue(request == verify_request)
    self.assertTrue(response == verify_response)
  
  def test_invalid_json(self):

  def test_invalid_request(self):

  def test_batch_invalid_json(self):
  
  def test_empty_array(self):

  def test_nonempty_array(self):
    

```

```
```

```
```
