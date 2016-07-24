# Building in Linux

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

# Building in Windows

Make sure the source code for SDL is in the same parent directory as this repo, i.e.:

```
./macemu/...
./SDL-1.2.15/...
```

Download SDL code from: https://libsdl.org/download-1.2.php then open it in VS 2015 to perform a one-way upgrade. Then open this project and build the "Release" target.
