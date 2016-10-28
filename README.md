Heroku buildpack: C++
===================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for C++ apps.
It uses [CMake](https://cmake.org/).

Usage
-----

Example usage:

    $ ls
    CMakeLists.txt myapp.c

    $ heroku create --stack cedar --buildpack http://github.com/d3roch4/heroku-buildpack-c.git

    $ git push heroku master
    ...
    -----> Heroku receiving push
    -----> Fetching custom buildpack
    -----> C app detected
    -----> Configuring
           Looking for somelibrary… ok
    -----> Compiling with Make
           gcc -o myapp myapp.c

The buildpack will detect your app as C/C++ if it has the file `CMakeLists.txt` in the root.  It will run a `cmake` command sucsses. It will then run `make` to compile the app.

Hacking
-------

To use this buildpack, fork it on Github.  Push up changes to your fork, then create a test app with `--buildpack <your-github-url>` and push to it.
