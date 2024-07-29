Fadecandy Server
================

The Fadecandy Server is a background process that handles the USB communications with one or more Fadecandy Controller boards.

You can send pixel data to a Fadecandy Server over the Open Pixel Control protocol, or from a web app via WebSockets. See the 'doc' directory for details on all protocols supported.

The Fadecandy Server optionally takes configuration options in the form of a JSON config file. Configuration files allow you to do things like:

* Support multiple Fadecandy boards
* Mix Fadecandy and DMX lighting devices
* Listen on an alternate TCP port
* Listen for connections from the network, not just from local programs

The configuration file format is documented in the **doc** directory.

When you run the Fadecandy Server, it will provide a simple web interface. By default, the Fadecandy server runs at [http://localhost:7890](http://localhost:7890).

Build
-----

It can build on Windows, Mac OS, or Linux using Make and other command line tools. On Windows, the build uses MinGW and gcc.

Windows NOT tested


Getting Started
---------------

In order to build the binary from source you need to run the following commands inside of the **server** directory:

this package depends upon libusb-1.0, and pkgconfig to find it

on OsX i tested macPorts, installing libusb-devel and pkgconfig.
if you have brew that's probably better, try that

after cloning the repo, remember to init the submodules
```bash
$ git submodule updat --init --recursive
```
to build it is
```bash
$ make
```

The compiled binary will be created in the same **server** directory

If you want to remove the compiled binary and source files run:

```bash
$ make clean
```
