# greple-docker

Dockernized [greple](https://github.com/kaz-utashiro/greple).

## Install

```sh
$ git clone https://github.com/ninoseki/greple-docker
$ cd docker
$ docker build -t greple .
```

## Usage

```sh
$ docker run greple
Usage:
    greple [-Mmodule] [ -options ] pattern [ file... ]

      PATTERN
        pattern              'and +must -not ?alternative &function'
        -e pattern           pattern match across line boundary
        -r pattern           pattern cannot be compromised
        -v pattern           pattern not to be matched
        --le pattern         lexical expression (same as bare pattern)
        --re pattern         regular expression
        --fe pattern         fixed expression
        --file file          file contains search pattern
...
```

This docker image comes with [greple-msdoc](https://github.com/kaz-utashiro/greple-msdoc) module.

```sh
$ docker -v /tmp:/tmp greple -Mmsdoc test /tmp/test.docx
```
