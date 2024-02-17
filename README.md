[unionfs-fuse-jsd](https://github.com/JavaScriptDude/unionfs-fuse-jsd)
============

This is a customized fork of the unionfs-fuse project that implements feature that notifies the caller of copy on write (COW) events for custom usecases where this information can be leveraged downstream.

This version is intended to be run in 'follow mode' (-f) so the invoking tool (eg Python) can read the stdout and trigger events off the COW notices.

For any standard unionfs applications, please use the excellent [unionfs-fuse] project by rpodgorny


How to build
------------

1. install packages

For debian systems:
```
    apt install make cmake libfuse3-dev libglib2.0-dev
```

2. cmake

```
mkdir build
cd build
cmake ..
make
```

This should allow for compilation on wider variety of systems (linux, macos, ...) and allows to enable/disable some features (xattrs, libfuse2/libfuse3, ...).

To see the list of all options, run `cmake -LAH` after the `cmake ..` step.

Example of option usage:

```
cmake .. -DWITH_LIBFUSE3=FALSE -DWITH_XATTR=FALSE
```