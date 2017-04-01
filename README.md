# Hug-et-al-Cell-2017-Supp-Site

Supplementary site for Hug CB, Grimaldi AG, Kruse K, Vaquerizas JM. (2017). Chromatin Architecture Emerges during Zygotic Genome Activation Independent of Transcription.

[doi:10.1016/j.cell.2017.03.024](http://dx.doi.org/10.1016/j.cell.2017.03.024)

All genomic coordinates are based on Flybase r6.07.

## Boundary calls

TAD Boundary calls are provided as BED files including the boundary score in the 4th column, higher values represent stronger boundaries. Calls where performed using Hi-C matrices at three different binning resolutions.

## Consensus boundary calls

Consensus boundary calls between developmental stages are provided as tab-separated text files. If boundaries at different stages were less than two bins away from each other they where considered to overlap and the median of the start and end coordinate were used as consensus boundary call. NA denotes boundaries not called or called with a score <0.5 at this stage.

