# rrm

`rrm` (Really Remove) is a Bash script for Unix-like systems (Linux, macOS, BSD) that overwrites a file's contents with null (0) bytes, then removes it from the file system, as if it was never there at all. This has some advantages, like more securely removing a file, and making compressed drive backups smaller. Only use `rrm` if you want to permanently scrub a file from your system!

Flags:
`-r` — recursively remove directories and their contents
`-v` — print removed files to terminal

`rrm` takes in any number of arguments, only works if both the file and the directory it's in have write access (bypass this with `sudo` if you dare), and stops if it encounters an error. A directory is removed by default if it's empty. A special file (e.g. a device file) is zeroed out without being removed.

To use `rrm` from anywhere, put it in a PATH directory (I use `~/bin`).
