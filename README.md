funblog
=====

## Intro

Attempt to use Docker to build/develop in funblog with GHC 8.0.1

See [funblog](https://github.com/agrafix/funblog)

## Does not work!

Installing GHC 8.0.1 fails.

To reproduce,
1. install [docker](http://www.docker.com)
2. clone this repo; and cd into it
3. ./run
   This will build image from haskell:8.0.1, although we plan to use local GHC, not the system-wide GHC in this container. It runs the container's /bin/bash, so you will be in a login shell.
4. Once in there, de 

```sh
root@..$ stack update
root@..$ stack setup 
```

This last step will download GHC 8.0.1 and try to build it. It fails with 'Too many files open'

## Credits

All credits to Alexander Thiemann; and all mistakes to me :-(
