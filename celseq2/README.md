###
Goals:
1. Build STAR index (done)
2. Make config.yaml file (done)
3. Create an experiment table
4. Run the celseq2 pipeline

## 
Commands:
mkdir dm6_ERCC_GAL4_GFP_STAR

screen
...
Ctrl-a Ctrl-d 
screen -list
screen -r

STAR --runThreadN 8 --runMode genomeGenerate --genomeDir dm6_ERCC_GAL4_GFP_STAR \
--sjdbGTFfile dm6.refGene.CEL-Seq.gtf --sjdbOverhang 49 --genomeFastaFiles dm6_ERCC_GAL4_GFP.fa

STAR --runThreadN 8 --runMode genomeGenerate --genomeDir dm6_ERCC_GAL4_GFP_STAR_noGTF \
--sjdbOverhang 49 --genomeFastaFiles dm6_ERCC_GAL4_GFP.fa