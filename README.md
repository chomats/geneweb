# GeneWeb

GeneWeb is an open source genealogy software written in OCaml. It comes
with a Web interface and can be used off-line or as a Web service.

## Build status

|            | Linux             | macOS             | Windows (mingw64)
| ---:       | :---:             | :---:             | :---:
| OCaml 4.05 | [![l405]][travis] | [![m405]][travis] | -
| OCaml 4.06 | [![l406]][travis] | [![m406]][travis] | -
| OCaml 4.07 | [![l407]][travis] | [![m407]][travis] | -
| OCaml 4.08 | [![l408]][travis] | [![m408]][travis] | -
| OCaml 4.09 | [![l409]][travis] | [![m409]][travis] | [![win-409]][appveyor]

[l405]:https://travis-matrix-badges.herokuapp.com/repos/geneweb/geneweb/branches/master/1
[l406]:https://travis-matrix-badges.herokuapp.com/repos/geneweb/geneweb/branches/master/2
[l407]:https://travis-matrix-badges.herokuapp.com/repos/geneweb/geneweb/branches/master/3
[l408]:https://travis-matrix-badges.herokuapp.com/repos/geneweb/geneweb/branches/master/4
[l409]:https://travis-matrix-badges.herokuapp.com/repos/geneweb/geneweb/branches/master/5
[m405]:https://travis-matrix-badges.herokuapp.com/repos/geneweb/geneweb/branches/master/6
[m406]:https://travis-matrix-badges.herokuapp.com/repos/geneweb/geneweb/branches/master/7
[m407]:https://travis-matrix-badges.herokuapp.com/repos/geneweb/geneweb/branches/master/8
[m408]:https://travis-matrix-badges.herokuapp.com/repos/geneweb/geneweb/branches/master/9
[m409]:https://travis-matrix-badges.herokuapp.com/repos/geneweb/geneweb/branches/master/10
[win-409]:https://ci.appveyor.com/api/projects/status/5a5yk7jvxk332pxu/branch/master?svg=true
[travis]:https://travis-ci.org/geneweb/geneweb
[appveyor]:https://ci.appveyor.com/project/geneweb/geneweb

## Documentation

The documentation is available online: http://geneweb.tuxfamily.org/

## Installation

Using [opam](https://opam.ocaml.org/):

```
opam pin add geneweb -k git https://github.com/geneweb/geneweb --no-action
opam depext geneweb
opam install geneweb
```

## Getting involved

We encourage you to participate in this open source project. We love
pull requests, bugs reports, ideas...

* Documentation: http://geneweb.tuxfamily.org/wiki/GeneWeb
* Mailing list: https://groups.yahoo.com/neo/groups/GeneWeb/info
* IRC: irc://irc.freenode.net/geneweb
* Git: https://github.com/geneweb/geneweb
* Forum: http://www.geneanet.org/forum/GeneWeb-85
* Facebook group: http://www.facebook.com/geneweb
* Wikipedia: https://en.wikipedia.org/wiki/GeneWeb

## Contributor guidelines

### Install dependencies

```
$ opam install camlp5 cppo dune markup ounit
```

### Build instructions

1. Run the configuration script
   ```
   $ ./configure
   ```
2. Build the distibution
   ```
   $ make clean distrib
   ```

### Building the API

The API uses the Google Protocol Buffer to exchange information
encoded as pb, json, xml.

Install [protoc](https://github.com/protocolbuffers/protobuf#protocol-compiler-installation),
and these extra dependencies:

```
$ opam install ocurl piqi piqilib redis redis-sync yojson
```

Then, tell the configure script to enable API.

```
$ ./configure --api
```

### Coding style

* Try to keep the same coding style as the existing one.
* New code should not contain any trailing whitespace.
* Each pull request should have a single clear purpose. If it containes
  multiple unrelated changes, those changes should be split into
  separate pull requests.
* If the PR needs to be update, push force.
* When submitting a new feature/function, write documentation and tests if it is relevant.

## Copyright

All files marked in this distribution are Copyright (c) 1998-2016 INRIA
(Institut National de Recherche en Informatique et Automatique) and
distributed under the GNU GENERAL PUBLIC LICENSE. See [LICENSE](LICENSE) file
for details.
