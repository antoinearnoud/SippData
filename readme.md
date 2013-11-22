

# SippData constructor scripts

This repository contains 

1. bash scripts to download SIPP raw data and stata do-file instructions to read the data into .dta format
2. modified versions of the do-files as supplied by [NBER](http://www.nber.org/data/survey-of-income-and-program-participation-sipp-data.html). The modification is small and only allows the scripts
   to be called inside a loop one after the other.

## useage

* you need a unix/macOS machine to run the bash scripts. (I think).
* downloads core and topical modules form SIPP
* The typical stata data for a panel has about 7GB
* the entire raw data is 50GB

Proceed like this:

1. run each of the setup_SIPPyy.sh scripts with `./setup_SIPPyy.sh` on your command line. This should download all the raw data
   into a folder structure I set up at `~/datasets/SIPP`. You can change that location by changing the variable `dest` inside the scripts
2. run each of the `makeyyyy.do` scripts in stata. this should read the raw data into stata format and apply the labels.

The bash scripts will check if a file exists, to avoid downloading large files again. if you think anything went wrong
during the process, just delete a folder in `~/datasets/SIPP` to recreate it.

Each panel has about 7GB in stata format


## Disclaimer

The usual disclaimer applies, i.e. I do not guarantee anything about this software. I hope it is useful and feel free to use it.

## Copyright

* The original do-files are all copyright NBER. Please see the link above.
