Instruction on running ezTree on the example genomes

Yu-Wei Wu (yuwei.wu@tmu.edu.tw)

In this folder you can find 23 genome files downloaded from NCBI along with six list files specifying different taxonomic lineages. Here are the steps to run the example files and get the phylogenetic trees from the list files.

1. Make sure the required software of ezTree is installed properly. Please refer to the README.txt in ezTree folder for more information.

2. The command to run ezTree for the six list files are (assuming ezTree script is located at ../)
   ../ezTree -list list_species -out list_species.out
   ../ezTree -list list_genus -out list_genus.out
   (...)
   ../ezTree -list list_phylum -out list_phylum.out


3. The results can be found at the specified output files. For example, the output for "-out list_species.out" are:
   - list_species.aln: the concatenated protein alignment file
   - list_species.aln.pfam: the marker genes
   - list_species.nwk: the tree in Newick format


