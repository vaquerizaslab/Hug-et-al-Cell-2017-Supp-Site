# Hug-et-al-Cell-2017-Supp-Site

Supplementary site for Hug CB, Grimaldi AG, Kruse K, Vaquerizas JM. (2017). Chromatin Architecture Emerges during Zygotic Genome Activation Independent of Transcription.

[doi:10.1016/j.cell.2017.03.024](http://dx.doi.org/10.1016/j.cell.2017.03.024)

All genomic coordinates are based on Flybase r6.07.

## Boundary calls

TAD Boundary calls are provided as BED files including the boundary score in the 4th column, higher values represent stronger boundaries. Calls where performed using Hi-C matrices at three different binning resolutions.

## Consensus boundary calls

Consensus boundary calls between developmental stages are provided as tab-separated text files. If boundaries at different stages were less than two bins away from each other they where considered to overlap and the median of the start and end coordinate were used as consensus boundary call. NA denotes boundaries not called or called with a score <0.5 at this stage.

## Processed Hi-C matrices

Hi-C matrices binned at 5kb resolution are available from [ArrayExpress E-MTAB-4918](https://www.ebi.ac.uk/arrayexpress/files/E-MTAB-4918/) in E-MTAB-4918.processed.1.zip and E-MTAB-4918.processed.2.zip. Reads from all replicates were merged to generate these matrices. They are provided in the [Cooler format](https://github.com/mirnylab/cooler) developed by the Mirny lab with matrix balancing information included in the file.

In order to extract the matrix in a flat text format, use:

```bash
cooler dump -t pixels --header -b --join -o 3-4h_repl_merged_5kb.tsv.gz 3-4h_repl_merged_5kb.cool
```

The flat file has the following records:

```
chrom1	start1	end1	chrom2	start2	end2	count	balanced
X	50000	55000	X	50000	55000	7	0.0271974
X	50000	55000	X	120000	125000	12	0.0238841
X	50000	55000	X	125000	130000	33	0.0209088
X	50000	55000	X	130000	135000	19	0.010838
X	50000	55000	X	135000	140000	22	0.0103313
X	50000	55000	X	140000	145000	21	0.013437
X	50000	55000	X	145000	150000	27	0.0119021
X	50000	55000	X	150000	155000	27	0.0132561
X	50000	55000	X	155000	160000	22	0.012156
```

