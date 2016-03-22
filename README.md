## par2deep

Analogous to the various *deep commands (md5deep, hasdeep...) this tool serves to create, verify and repair parity files in an entire directory hierarchy.

This tool will generate one parity file (plus a file for the recovery blocks) per file that you protect. This makes it simple to move files if you change your mind on how your file tree must be organized. Just move the `par2` files along.

## Motivation
I chose to use the old but well tested and well known `par2` program to base this tool on, instead of similar tools such as `zfec`, `rsbep` or something like `pyFileFixity`. Some recent forks of `par2` have added recursive scanning abilities, but they're generally not cross-platform.

I use `par2deep` to secure my photos and music across drives, machines and operating systems, and I intend to keep securing my data this way in the decades to come. I felt that the wide availability of the `par2` tool was my best bet.

### Install

Simply run the following:

    $ python setup.py install

Or run directly with:

    $ python par2deep

## Usage

After installation, run with `par2deep`. Command line options may be enumerated by using the --help option.

## Dependencies

 * tqdm
 * glob2
 * `par2` in path or specify a tool with the same interface.

### Changelog

2016-03-22: Finish port to Python 3, added setup.py.
2016-03-19: Added quiet mode, keep backup files upon unsuccesful repair.
2016-03-17: First release