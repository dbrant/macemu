# Notes

Make sure to first install these packages:

```
$ sudo apt-get install autoconf
$ sudo apt-get install xorg-dev
```

To build BasiliskII:

```
$ cd ./BasiliskII/src/Unix
$ sh autogen.sh
$ make
```

To build SheepShaver:

```
$ cd ./SheepShaver/src/Unix
$ sh autogen.sh
$ make
```

If you get build errors related to the stack-checker, build with the following parameters:

```
$ make clean
$ sh autogen.sh
$ CXXFLAGS="-fno-stack-protector -g -O2" CFLAGS="-fno-stack-protector -O2" ./autogen.sh
```
