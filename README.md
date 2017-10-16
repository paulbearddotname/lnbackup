# lnbackup

lnbackup is a backup program capable of creating backup directories that mirror the source without duplicating unmodified files.

Each run results in a new backup directory named with the date and time the backup started.
Each backup directory is a complete mirror of the source.
Unmodified backup files are hard linked.
New backup files are created as copy-on-write duplicates of source files if possible.
Files are also indexed by hash to identify moved, renamed, and duplicate files.

Slower but more space efficient than [rsyncbackup](../../../rsyncbackup).

## See also

[rsyncbackup](../../../rsyncbackup)

## Website

http://paulbeard.name

## Install

    sudo install lnbackup /usr/local/bin/
