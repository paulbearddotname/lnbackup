# lnbackup

lnbackup is a backup program capable of creating backup directories that mirror the source without duplicating unmodified files.

Each run results in a new backup directory named with the date and time the backup started.
Each backup directory is a complete mirror of the source.
Unmodified backup files are hard linked.
New backup files are created as copy-on-write duplicates of source files if possible.
Files are also indexed by hash to identify moved, renamed, and duplicate files.

## Website

https://paulbeard.name

## Install

    sudo install lnbackup /usr/local/bin/

## Help

    $ lnbackup -h
    lnbackup version 1.2.0
    Copyright (c) 2021 Paul Beard.
    Website: paulbeard.name

    lnbackup is a backup program capable of creating backup directories that mirror the source without duplicating unmodified files.

    Usage: /usr/local/bin/lnbackup [-h] SRC_FROM DEST

    Options:
     -h       show this help
     SRC_FROM read source list from file
     DEST     destination directory
