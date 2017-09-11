# SYNOPSIS

Select lines between two patterns using awk.

The author of original awk script is [fedorqui](https://stackoverflow.com/users/1983854/fedorqui)
the code is taken from [StackOverflow](https://stackoverflow.com/a/38972737/5147708).


# INSTALL

    $ sparrow plg install awk-select-lines


# USAGE

To print lines betwenn two patterns (`$pat1` and `$pat1`) in `$file`:

    $ sparrow plg run awk-select-lines \
    --param file=/path/to/file/example.txt \
    --format concise --param pat1=PAT1 --param pat2=PAT2 \
    --param mode=2

Setting mode:

`Mode` parameter define the selection logic, based on explnation taken from

[https://stackoverflow.com/a/38972737/5147708](https://stackoverflow.com/a/38972737/5147708)


* `mode=1` (default mode) - Print lines between PAT1 and PAT2
* `mode=2` - Print lines between PAT1 and PAT2 - not including PAT1 and PAT2
* `mode=3` - Print lines between PAT1 and PAT2 - including PAT1
* `mode=4` - Print lines between PAT1 and PAT2 - including PAT2
* `mode=5` - Print lines between PAT1 and PAT2 - excluding lines from the last PAT1 to the end of file if no other PAT2 occurs

# Plugin maintainer

Alexey Melezhik

# Prerequisites

Awk should be installed


