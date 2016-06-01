RNA Bioinformatics Crash Course
-----------------------------------

(under development)

TODO:

- use data from Rhiju!

The sequence:

    GGAUCACGAGGGGGAGACCCCGGCAACCUGGGACGGACACCCAAGGUGCUCACACCGGAGACGGUGGAUCCGGCCCGAGAGGGCAACGAAGUCCGU

# 1. Sequence
What is a FASTA format? 

- [ ] 1. write the seq in the Fasta format

More: https://en.wikipedia.org/wiki/FASTA_format

**RFAM** database is a collection of RNA families, each represented by multiple sequence alignments, consensus secondary structures and covariance models (CMs). (http://rfam.xfam.org/)

- [ ] 2. Which RNA family the seq belongs to?
- [ ] 3. How many structures 
- [ ] What members clan (CL00012) contains?

# 2. Secondary structure prediction
Predict secondary structure for the sequence:

http://genesilico.pl/comparna/
## Get ss from a structure (in the PDB format)


# 3. Predict the structure using SimRNAweb/RNAComposer/MC-SYM|MC-Fold
<http://iimcb.genesilico.pl/SimRNAweb/>
# 4. Assess the quality of your structure with mqapRNA
<http://mqaprna-vm.dmz.genesilico.pl:8666/>
# 5. Calculate RMSD between A and B

# Formats

Which format to save:

- [ ] a sequence
- [ ] a secondary structure
- [ ] a structure.

# Restrants
https://rmdb.stanford.edu/browse/
# RNA utils
## ModeRNA - a program for comparative RNA modeling
http://genesilico.pl/moderna/
## ClaRNA
## RNA Bricks
http://iimcb.genesilico.pl/rnabricks/

## NPDock - protein-RNA/DNA docking
http://genesilico.pl/NPDock/

## QRNAS - structure refinement
QRNA 0.2 - Quick Refinement of Nucleic Acids 0.2

Tutorial by Magnus https://docs.google.com/document/d/1ccbsZrnafBHJGEuXR2lvvMSh49VdTZMZfnyy0NFZxO8/edit

QRNA [RNA&DNA ONLY (incl. modified nts)

- adds missing atoms (esp. hydrogen)
- single-point energy calculations
- energy minimization in all-atom representation (Amber ff ONLY, implicit water, constraints possible)

https://docs.google.com/document/d/1ccbsZrnafBHJGEuXR2lvvMSh49VdTZMZfnyy0NFZxO8/edit

    $ ./QRNA -i pdbfile.pdb -o outfile.pdb
    It minimizes pdbfile.pdb and writes outfile.pdb every 100 steps. 
    All default parameters are used, which should be fine in most cases.

# Scientific software
## Biopython
The Biopython Project is an open-source collection of non-commercial Python tools for computational biology and bioinformatics, created by an international association of developers. It contains classes to represent biological sequences and sequence annotations, and it is able to read and write to a variety of file formats. It also allows for a programmatic means of accessing online databases of biological information, such as those at NCBI. Separate modules extend Biopython's capabilities to sequence alignment, protein structure, population genetics, phylogenetics, sequence motifs, and machine learning. Biopython is one of a number of Bio* projects designed to reduce code duplication in computational biology.

- [ ] read a seq.fa into biopython
- [ ] calc rmsd between two structures using biopython

More:

- https://en.wikipedia.org/wiki/Biopython
- http://biopython.org/wiki/Getting_Started
## Pandas
Pandas is a software library written for the Python programming language for data manipulation and analysis. In particular, it offers data structures and operations for manipulating numerical tables and time series. Pandas is free software released under the three-clause BSD license.[2] The name is derived from the term "panel data", an econometrics term for multidimensional structured data sets.

More:

- https://en.wikipedia.org/wiki/Pandas_%28software%29
- http://pandas.pydata.org/pandas-docs/version/0.18.1/10min.html

Practicals:

- [ ] make an dataframe, `df2` and run head(), tail(), and select a column

## NumPy
NumPy (pronounced "Numb Pie" or sometimes "Numb pee"[1][2]) is an extension to the Python programming language, adding support for large, multi-dimensional arrays and matrices, along with a large library of high-level mathematical functions to operate on these arrays. The ancestor of NumPy, Numeric, was originally created by Jim Hugunin with contributions from several other developers. In 2005, Travis Oliphant created NumPy by incorporating features of the competing Numarray into Numeric, with extensive modifications. NumPy is open source and has many contributors.

More:

- https://en.wikipedia.org/wiki/NumPy
- http://www.numpy.org/
- https://docs.scipy.org/doc/numpy-dev/user/quickstart.html

Practicals:

- [ ] make an array of [2,3,1,0]
- ...

## Matplotlib
matplotlib is a plotting library for the Python programming language and its numerical mathematics extension NumPy. It provides an object-oriented API for embedding plots into applications using general-purpose GUI toolkits like wxPython, Qt, or GTK+. There is also a procedural "pylab" interface based on a state machine (like OpenGL), designed to closely resemble that of MATLAB. SciPy makes use of matplotlib. matplotlib was originally written by John D. Hunter, has an active development community, and is distributed under a BSD-style license. Michael Droettboom was nominated as matplotlib's lead developer shortly before John Hunter's death in 2012.

https://en.wikipedia.org/wiki/Matplotlib

Practicals:

- [ ] plot [2,3,1,0]
- ...

## SciKit
## IPython Notebook (Jupyter)
The IPython Notebook is now known as the Jupyter Notebook. It is an interactive computational environment, in which you can combine code execution, rich text, mathematics, plots and rich media. For more details on the Jupyter Notebook, please see the Jupyter website.

https://ipython.org/notebook.html
## PyMOL
- http://www.pymolwiki.org/index.php/Practical_Pymol_for_Beginners
- http://csb.stanford.edu/class/public/pages/sykes_pymol/pymol_info.html

Practicals:

- select a chain by clicking and from the cmd
- renumber a chain
- show a structure as cartoon and ribbon
- align two structures

# Utils
## Python
### subprocess
err = subprocess.call(cmd, shell=True)
## Terminal
The system console, computer console, root console, operator's console, or simply console is the text entry and display device for system administration messages, particularly those from the BIOS or boot loader, the kernel, from the init system and from the system logger. It is a physical device consisting of a keyboard and a screen, and traditionally is a text terminal, but may also be a graphical terminal. System consoles are generalized to computer terminals, which are abstracted respectively by virtual consoles and terminal emulators. Today communication with system consoles is generally done abstractly, via the standard streams (stdin, stdout, and stderr), but there may be system-specific interfaces, for example those used by the system kernel.

Practicals:

- [ ] show the contect of seq.fa file in your terminal
- [ ] change permission to execute to this file (just doesn't make any sense)
- [ ] install biopython/pymol from using terminal
- [ ] login to a remote machine using ssh keys
- [ ] mount a drive using sshfs
- [ ] download from the terminal this file http://files.rcsb.org/download/1XJR.pdb
- [ ] check the version of your system
- [ ] add this `~/bin/` to your (python) path and reload the file with a new variable
- [ ] grep a file...
- [ ] open a seq.fa in vim and quite ;-)
- [ ] take a look at the processes at your machine? (htop)
- [ ] write a simple bash script to run `cat seq.fa`
- [ ] go to your home and find `seq.fa`
- [ ] gzip `seq.fa`
- [ ] get the top of `seq.fa`
- [ ] get the bottom of `seq.fa`
- [ ] screen?
- [ ] diff?
- [ ] rsync?
- [ ] crontab?
- [ ] run mc and move to your home
- [ ] http://www.skamphausen.de/cgi-bin/ska/CDargs ?
- [ ] make an alias

https://en.wikipedia.org/wiki/System_console
## Cluster

magnus@peyote2:~$ qstat -u '*'

	for i in `seq -w 1 10`; do echo "../SimRNA -c config.dat -s 1gid.fas -S 1gid.ss -r 1gid_restraints_3_01.txt -E 10 -R $i -o 1gid+restraints_3_01_$i >& 1gid+restraints_3_01_$i.txt" | qsub -cwd -V -pe mpi 10 -l h_vmem=250M; done

## Git
Git (/ɡɪt/) is a version control system that is widely used for software development and other version control tasks. It is a distributed revision control system with an emphasis on speed, data integrity, and support for distributed, non-linear workflows.[9] Git was created by Linus Torvalds in 2005 for development of the Linux kernel, with other kernel developers contributing to its initial development.

<https://gitlab.genesilico.pl/Tutorials/git_crash_course> (private)

https://en.wikipedia.org/wiki/Git_%28software%29
# More

- https://ribokit.github.io/
- https://daslab.stanford.edu/resources/

## RNA motifs
https://en.wikipedia.org/wiki/Tetraloop

# References

Rfam 12.0: updates to the RNA families database. Eric P. Nawrocki, Sarah W. Burge, Alex Bateman, Jennifer Daub, Ruth Y. Eberhardt, Sean R. Eddy, Evan W. Floden, Paul P. Gardner, Thomas A. Jones, John Tate and Robert D. Finn Nucleic Acids Research (2014)  10.1093/nar/gku1063 
