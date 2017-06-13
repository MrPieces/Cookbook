Compiling ArangoDB
==================

Problem
-------

You want to modify sources or add your own changes to ArangoDB.

Solution
--------

Arangodb, as many other opensource projects nowadays is standing on the shoulder of giants.
This gives us a solid foundation to bring you a uniq feature set, but it introduces a lot of
dependencies that need to be in place in order to compile arangodb.

Since build infrastructures are very different depending on the target OS, choose your target
from the recepies below.

- [Compile on Debian](Debian.md)

- [Compile on Windows (3.x)](Windows30.md)

- [Compile on Windows (2.x)](Windows.md)

- [Compile on Windows (pre-2.4)](WindowsLegacy.md)

- [Running Custom Build](RunningCustomBuild.md)

  - [Recompiling jemalloc](jemalloc.md)

  - [OpenSSL 1.1](OpenSSL.md)
