# High Performace Computing

Researchers are more and more likely to need to analyze raw data sets using some sort of analysis process before they can be interpreted in the context of the scientific question. Raw data, whether from an array or sequencing for example, are not typically directly interpretable results, thus require some degree of processing. The nature of the processing depends on the data type, the platform with which the data were generated, and the biological question being asked of the data set.

## Architecture

To that end we use a serverless cloud computing architecture based on AWS Batch, Step Fuctions, and an ECR computing cluster; to process raw data which output datasets that can be analyzed. Below is a general outline of our computing cluster.

![Architecture](/assets/tubio-hpc-compute-environment.png)

## AWS Batch

We currenty have Batch Job definitions for the following tools:

| Tool        | Version       | Project Homepage                                          |
| ----------- | ------------- |-----------------------------------------------------------|
| Amos        | 3.1.0         | [https://sourceforge.net/projects/amos/](https://sourceforge.net/projects/amos/)                    |
| BBTools     | 38.92         | [https://jgi.doe.gov/data-and-tools/bbtools/](https://jgi.doe.gov/data-and-tools/bbtools/)               |
| BCFTools    | 1.9           | [http://samtools.github.io/bcftools/howtos/install.html](http://samtools.github.io/bcftools/howtos/install.html)    |
| BWA-Mem2    | 2.2.1         | [https://github.com/lh3/bwa](https://github.com/bwa-mem2/bwa-mem2) |
| CDHit       | 4.8.1         | [https://github.com/weizhongli/cdhit](https://github.com/weizhongli/cdhit) |
| CheckM      | 2.6.1         | [https://ecogenomics.github.io/CheckM/](https://ecogenomics.github.io/CheckM/) |
| Concoct     | 1.1.0         | [https://github.com/BinPro/CONCOCT](https://github.com/BinPro/CONCOCT) |
| Fastp       | 0.22.0        | [https://github.com/OpenGene/fastp](https://github.com/OpenGene/fastp) |
| Fastqc      | 0.11.9        | [https://www.bioinformatics.babraham.ac.uk/projects/fastqc/](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/) |
| Maxbin2     | 2.2.7         | [https://sourceforge.net/projects/maxbin2](https://sourceforge.net/projects/maxbin2) |
| Megahit     | 1.2.9         | [https://github.com/voutcn/megahit](https://sourceforge.net/projects/maxbin2) |
| Metabat     | 2.15          | [https://bitbucket.org/berkeleylab/metabat](https://bitbucket.org/berkeleylab/metabat) |
| Metaquast   | 5.0.2         | [https://sourceforge.net/projects/quast](https://sourceforge.net/projects/quast) |
| Samtools    | 1.9           | [http://www.htslib.org/doc/samtools.html](http://www.htslib.org/doc/samtools.html) |
| Spades      | 3.15.3        | [http://cab.spbu.ru/software/spades/](http://cab.spbu.ru/software/spades/) |
