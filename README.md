MetaSV
===========

MetaSV: An accurate and integrative structural-variant caller for next generation sequencing

# Software Dependencies
MetaSV uses the following Python packages which must be available on the `PYTHONPATH` environment variable:
* [pysam](http://pysam.readthedocs.org/en/latest/): Only version 0.7.7 has been tested to work with MetaSV
* [pybedtools](http://pythonhosted.org/pybedtools/): Note that [bedtools](https://github.com/arq5x/bedtools2) (version 2.21 or greater) has to be installed separately in order for pybedtools to work.
* [pyvcf](https://github.com/jamescasbon/PyVCF)

In addition, it requires the following software to be installed:
* [SPAdes](http://bioinf.spbau.ru/spades): Use for assembly around the SV breakpoints
* [AGE](https://github.com/abyzovlab/AGE): Used for determining the SV breakpoints using assembled contigs. Please use AGE code from the following [fork](https://github.com/marghoob/AGE/archive/simple-parseable-output.zip) of the main repository--the code was modified to make AGE output simpler to parse. This dependency on the fork will be fixed in the next release.

The paths to the above tools are specified on the command-line options for MetaSV.

# Tools
* `metasv.py`: Top-level MetaSV script. Use this when running all of MetaSV.
* `breakdancer_reader.py`: Reader for BreakDancer output files. Can also convert to a VCF file.

# Installing
`pip install https://github.com/bioinform/metasv/archive/<version>-alpha.tar.gz`. The current version of MetaSV is 0.1-alpha.

# Running
Type `metasv.py -h` for help on the command-line options.

