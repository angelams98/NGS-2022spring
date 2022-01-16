# NGS-2022spring

Possibly subsample

Remove adapters and quality control (AdapterRemoval, Trimmomatic, cutadapt, fastp)

Align reads to reference genome, fastq → bam (BWA mem)

Mark duplicates (Picard)

Get variants from alignment, bam → vcf (GATK HaplotypeCaller)

Inspect mutations in the pncA gene including a potential deletion

Construct a phylogenetic tree, vcf → fasta → phylip(phyml)

Visualize the phylogenetic tree (iTOL)

Do PCA analysis to check possible clusters (R)

Predict drug resistance (TB-profiler)


nice -n 19 java -jar /usr/local/bin/picard.jar MarkDuplicates -I sorted/ERR3335${IND}_sort.bam -M picard/ERR3335${IND}.markdup.metrics.txt -O picard/ERR3335${IND}.markdup.bam
