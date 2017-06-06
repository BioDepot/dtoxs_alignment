# dtoxs_alignment

The container is used to do the alignment steps and is used in conjunction with biodepot/detox_analysis container to produce the final list of differentially expressed genes.

Due to the large sizes, the reference files and fastq files are not included with the container. They need to be provided separately on the host running Docker and then mounted so that they can be seen by the container.

To run:

docker run --rm --name detoxs -v <referencedirectory>:/root/LINCS/References/Broad_UMI /Human_RefSeq/ -v <fasttq sequence directory>:/root/LINCS/Seqs biodepot/dtoxs_alignment /root/LINCS/Programs/Broad-DGE/run-alignment-analysis.sh
