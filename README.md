RNA Bioinformatics Crash Course
-----------------------------------

(under development)

TODO:

- use data from Rhiju!

The sequence:

    GGAUCACGAGGGGGAGACCCCGGCAACCUGGGACGGACACCCAAGGUGCUCACACCGGAGACGGUGGAUCCGGCCCGAGAGGGCAACGAAGUCCGU

# 1. Sequence
What is a FASTA format? 

- 1. [ ] write the seq in the Fasta format

More: https://en.wikipedia.org/wiki/FASTA_format
## Which RNA family the seq belongs to?

- [ ] Which RNA family the seq belongs to?
# 2. Secondary structure prediction
Predict secondary structure for a sequence:

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
## biopython

- [ ] 
## pandas
## numpy
# Utils
## Terminal
The system console, computer console, root console, operator's console, or simply console is the text entry and display device for system administration messages, particularly those from the BIOS or boot loader, the kernel, from the init system and from the system logger. It is a physical device consisting of a keyboard and a screen, and traditionally is a text terminal, but may also be a graphical terminal. System consoles are generalized to computer terminals, which are abstracted respectively by virtual consoles and terminal emulators. Today communication with system consoles is generally done abstractly, via the standard streams (stdin, stdout, and stderr), but there may be system-specific interfaces, for example those used by the system kernel.

- [ ] show the contect of seq.fa file in your terminal
- [ ] change permission to execute to this file (just doesn't make any sense)
- [ ] install biopython/pymol from using terminal
- [ ] login to a remote machine using ssh keys
- [ ] mount a drive using sshfs
- [ ] download from the terminal this file http://files.rcsb.org/download/1XJR.pdb
- [ ] check the version of your system
- [ ] add this `~/bin/` to your (python) path
- [ ] grep a file...
- [ ] open a seq.fa in vim and quite ;-)
- [ ] screen ...
- [ ] take a look at the processes at your machine? (htop)
- [ ] write a simple bash script to run `cat seq.fa`

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
