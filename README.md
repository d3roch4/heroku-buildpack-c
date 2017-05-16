Heroku buildpack: C++
===================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for C++ apps.
It uses [CMake](https://cmake.org/).

Usage
-----

Example usage:

    $ ls
    make.sh CMakeLists.txt myapp.c

    $ heroku create --stack cedar --buildpack http://github.com/d3roch4/heroku-buildpack-make.git

    $ git push heroku master
    ...


