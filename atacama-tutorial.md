# Atacama soil microbiome tutorial

## Setup

First, we are going to make a directory for our tutorial, as well as a directory for our raw, paired-end sequences.
mkdir = make a directory (folder)
cd = change directory

```
mkdir qiime2-atacama-tutorial
cd qiime2-atacama-tutorial
```
Then, we are going to download the sample metadata file and take a look at it.

```
wget \
  -O "sample-metadata.tsv" \
  "https://data.qiime2.org/2021.2/tutorials/atacama-soils/sample_metadata.tsv"
```

Next, you’ll download the multiplexed reads. We are going to put these in it's own directory. You will download three fastq.gz files, corresponding to the forward, reverse, and barcode (i.e., index) reads. These files contain a subset of the reads in the full data set generated for this study, which allows for the following commands to be run relatively quickly, however, we will perform additional subsampling in this tutorial to further improve the run time.

```
mkdir emp-paired-end-sequences
cd emp-paired-end-sequences
```

```
wget \
  -O "emp-paired-end-sequences/forward.fastq.gz" \
  "https://data.qiime2.org/2021.2/tutorials/atacama-soils/10p/forward.fastq.gz"
```

```
wget \
  -O "emp-paired-end-sequences/reverse.fastq.gz" \
  "https://data.qiime2.org/2021.2/tutorials/atacama-soils/10p/reverse.fastq.gz"
```

```
wget \
  -O "emp-paired-end-sequences/barcodes.fastq.gz" \
  "https://data.qiime2.org/2021.2/tutorials/atacama-soils/10p/barcodes.fastq.gz"
```
