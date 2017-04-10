ezTree README

Yu-Wei Wu (yuwei.wu@tmu.edu.tw)
Graduate Institute of Biomedical Informatics, Taipei Medical University

[Introduction]
This script is used to get single copy marker genes from a set of genomes, including genome bins recovered from metagenomes, and align them for phylogenetic tree reconstruction.

[Prerequisite]
This script needs the following additional software tools.
  -HMMER3
  -muscle
  -Gblocks
  -Prodigal
  -FastTree

(If you already have the software installed in your system and have put them in system path, ezTree will attempt to run them directly. It will only complain that it cannot find the software if the software cannot be executed.)

(You can try running ezTree first, which will tell you what software are missing)

Installation guide:
  - HMMER3
    * Download the latest distribution from http://hmmer.org/. Assuming that we get version 3.1b2.
    * Unzip the tar.gz file using "tar zxvf hmmer-3.1b2-linux-intel-x86_64.tar.gz
    * cd (hmmer folder)
    * ./configure
    * make
    * cd src;pwd
    * Copy the path and enter it in the HMMER3 field of the "setting" file

  - muscle
    * Download the latest distribution from http://www.drive5.com/muscle/downloads.htm. Assuming that we get version 3.8.31.
    * Unzip the tar.gz file using "tar zxvf muscle3.8.31_i86linux64.tar.gz"
    * rename the muscle executable into muscle by "mv muscle3.8.31_i86linux64 muscle" or create symbolic link through "ln -s muscle3.8.31_i86linux64 muscle"
    * pwd
    * Copy the path and enter it in [MUSCLE] field of the "setting" file

  - Gblocks
    * Download the latest distribution from http://molevol.cmima.csic.es/castresana/Gblocks.html. Assuming we get version 0.91b.
    * Unzip the tar.Z file using "tar zxvf Gblocks_Linux64_0.91b.tar.Z"
    * Run "cd Gblocks_0.91b;pwd"
    * Copy the path and enter it in [GBLOCKS] field of the "setting" file

  - prodigal
    * Download the latest distribution from https://github.com/hyattpd/prodigal/releases/. Assuming we get version 2.63 linux distribution.
    * Change running permission by "chmod +x prodigal.linux"
    * Rename the prodigal executable into prodigal by "mv prodigal.linux prodigal" or create symbolic link through "ln -s prodigal.linux prodigal"
   * pwd
   * Copy the path and enter it in [PRODIGAL] field of the "setting" file

  - FastTree
    * Download the latest distribution from http://www.microbesonline.org/fasttree/#Install. Assuming we get version 2.1.9.
      ( If you get openmp version, either rename FastTreeMP into FastTree or create a symbolic link)
    * Change running permission by "chmod +x FastTree"
    * pwd
    * Copy the path and enter it in [FASTTREE] field of the "setting" file


ezTree also needs the latest PFAM hmm file, which will be downloaded automatically while running ezTree. Users may also elect to create "data" directory at ezTree folder and put the latest Pfam hmmer file inside.

[Usage]
  ezTree
    -list (list file of genomes)
    -out (output header)
   (Either -list or -dir is required for running ezTree)

   (Other parameters)
    [-thread (thread num; default 4)]
    [-evalue (evalue for HMMER; default 1e-10)]



[Example]
  ezTree -list genome.list -out genome.out
  ezTree -list genome.list -out genome.out -thread 8
  ezTree -list genome.list -out genome.out -thread 8 -evalue 1e-5

(Please refer to the MANUAL.pdf for an example about downloading genomes, creating list file, and run the script)



[LICENSE]
    ezTree -- a script for getting marker protein alignment from a set of genomes.
    Copyright (C) 2016  Yu-Wei Wu

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.

