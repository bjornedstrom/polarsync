# polarsync

Work in progress, a bit buggy.

This program can download data from the Polar M400 watch. It will write the raw outputs to a directory.

## Build

Requires `pyusb`.

    protoc --python_out=. polar.proto

## Install

On Linux it is advised to add udev rules to avoid having to run this program as root. See the `etc` directory for an example.

## Run

    mkdir syncdir
    PYTHONPATH=. ./polarsync -o syncdir

# About & License

Copyright (c) Björn Edström <be@bjrn.se> 2017. See LICENSE for details

The low level wire format parsing is inspired by v800_downloader by Christian Weber: https://github.com/profanum429/v800_downloader. See `polarsync` for details.
