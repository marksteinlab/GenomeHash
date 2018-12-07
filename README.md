# GenomeHash

## Featured in pre-print https://www.biorxiv.org/content/early/2018/12/04/485300

Repo for GenomeHash program, mirror of https://sourceforge.net/projects/genomehash/files/


The genomehashpackage contains 9 zip files:
	programs.zip
	apis.zip
	fly.zip
	fugu.zip
	mosquito.zip
	plant.zip
	rice.zip
	worm.zip
	yeast.zip

The first file, programs.zip, contains all the files necessary to build
enhancer.exe, which is the program that searches genomes for clusters. The
makefile make.enhancer directs the construction of enhancer.exe. Also in
programs.zip are all the files needed to construct makechrmutr.exe, which
is the program that converts the  NCBI .gbk files into the format neede
for the enhancer program

Each of the remaining eight files contain all the information about its
eponymous genome, as produced by makechrmutr from the genome's .gbk files 
at NCBI. Also included in each genome's zip file is a copy of
enhancer.exe constructed to run on a modern MAC. If you are running on a
different platform, construct enhancer.exe from the programs.zip file.

Each genome directory contains in .txt files, the data for that genome.

The master.txt file gives the names of the chromosomes of the organism, as
well as the informal name of the organism itself.

The datasize.txt file gives the sizes of various structures used to
represent the genome. It is used to allocate the correct amount of memory
to these structures.

The xallnames.txt file gives the names and synonyms for all the genes of the
genome.

The datasize.txt file gives the sizes of various structures used to
represent the genome. It is used to allocate the correct amount of memory
to these structures.

The xallnames.txt file gives the names and synonyms for all the genes of the
genome.

The file xchrdata.txt lists all the genes of the genome, and where in the 
condensed genome.txt file the DNA for that gene resides.

The genome.txt file gives the sequence of nucleotides in the genome, encoded
2 bits per nucleotide.
 
The exceptions.txt file lists all the locations where an N was specified in the
NCBI version of the genome. Since only two bits are used per nucleotide, these
N's appear to be the nucleotide A. But use of the exception file enables the
enhancer program to ignore any matches that utilize N's the the NCBI version
of the genome.

The file xcontigs.txt tells where each contig (.gbk file) is mapped into the
final genome, and which chromosome is represented. In some genomes, a 
chromosome is represented by several contigs, but in these eight genomes, each
chromosome is represented by one contig.

The xallnames.txt file gives all the names of the genes in the genome. Each 
entry contains a name and the gene number. Most genes have several recognized
names.

The utrinfo.txt file is not used in the current enhancer program. It is 
there for possible future use.

The file enhancer.exe is an executable file of the enhancer program 
constructed to run on a MAC.  It is exactly the file which would be
built from the code in the programs directory. You may have to issue the 
command "chmod a+x enhancer.exe" to make it executable, as some versions of
unzip remove the executable permission for reasons of security.
