Changelog
---------

3.0
...

* Added compatibility with Python 3.5.

* Refreshed documentation.

2.6
...

* Added ``local_address`` and ``remote_address`` attributes on protocols.

* Closed open connections with code 1001 when a server shuts down.

* Avoided TCP fragmentation of small frames.

2.5
...

* Improved documentation.

* Provided access to handshake request and response HTTP headers.

* Allowed customizing handshake request and response HTTP headers.

* Supported running on a non-default event loop.

* Returned a 403 error code instead of 400 when the request Origin isn't
  allowed.

* Cancelling :meth:`~websockets.protocol.WebSocketCommonProtocol.recv` no
  longer drops the next message.

* Clarified that the closing handshake can be initiated by the client.

* Set the close status code and reason more consistently.

* Strengthened connection termination by simplifying the implementation.

* Improved tests, added tox configuration, and enforced 100% branch coverage.

2.4
...

* Added support for subprotocols.

* Supported non-default event loop.

* Added ``loop`` argument to :func:`~websockets.client.connect` and
  :func:`~websockets.server.serve`.

2.3
...

* Improved compliance of close codes.

2.2
...

* Added support for limiting message size.

2.1
...

* Added ``host``, ``port`` and ``secure`` attributes on protocols.

* Added support for providing and checking Origin_.

.. _Origin: https://tools.ietf.org/html/rfc6455#section-10.2

2.0
...

* Backwards-incompatible API change:
  :meth:`~websockets.protocol.WebSocketCommonProtocol.send`,
  :meth:`~websockets.protocol.WebSocketCommonProtocol.ping` and
  :meth:`~websockets.protocol.WebSocketCommonProtocol.pong` are coroutines.
  They used to be regular functions.

* Added flow control.

1.0
...

* Initial public release.