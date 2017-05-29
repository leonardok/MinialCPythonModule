# Minimal C module for python

This code was based on https://en.wikibooks.org/wiki/Python_Programming/Extending_with_C, I just did include the CMakeLists for cmake compilation.

## Instructions

Using distutils
```
$ python setup.py build
$ python
>>> import hello
>>> hello.say_hello("World")
```

Using CMake
```
$ mkdir build   # to create a build dir
$ cd build
$ cmake ..      # create config for the root dir
$ make          # compile
$ python
>>> import hello
>>> hello.say_hello("World")
```