#plascad：predict plasmid
plascad -i 23cg223-contig52.fasta

#prokka：annote the bacteria genome
prokka --metagenome  --kingdom Bacteria --force  --cpus 60 --outdir 23cg223-contig52-MOBV --prefix 23cg223-contig52-MOBV  23cg223-contig52.fasta

#fastANI:caculate the ANI between the genomes
fastANI -q genome genome_B.fasta -r genome genome_B2.fasta  -o out_fastani
