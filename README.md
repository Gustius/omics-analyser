# nf-core/omics-analyser
**This pipeline uses four(?) different methods to analyse omics-data.**

[![Build Status](https://travis-ci.org/nf-core/omics-analyser.svg?branch=master)](https://travis-ci.org/nf-core/omics-analyser)
[![Nextflow](https://img.shields.io/badge/nextflow-%E2%89%A50.32.0-brightgreen.svg)](https://www.nextflow.io/)

[![install with bioconda](https://img.shields.io/badge/install%20with-bioconda-brightgreen.svg)](http://bioconda.github.io/)
[![Docker](https://img.shields.io/docker/automated/nfcore/omics-analyser.svg)](https://hub.docker.com/r/nfcore/omics-analyser)
![Singularity Container available](
https://img.shields.io/badge/singularity-available-7E4C74.svg)

## Introduction
The pipeline is built using [Nextflow](https://www.nextflow.io), a workflow tool to run tasks across multiple compute infrastructures in a very portable manner. It comes with docker / singularity containers making installation trivial and results highly reproducible.


## Documentation
The nf-core/omics-analyser pipeline comes with documentation about the pipeline, found in the `docs/` directory:

1. [Installation](docs/installation.md)
2. Pipeline configuration
    * [Local installation](docs/configuration/local.md)
    * [Adding your own system](docs/configuration/adding_your_own.md)
3. [Running the pipeline](docs/usage.md)
4. [Output and how to interpret the results](docs/output.md)
5. [Troubleshooting](docs/troubleshooting.md)


# Report
by Gust Verstraete

## Introduction

	History of data and bioinformatics, boom of data and omics, also about git and open-soucre
With the introduction of increasingly cheaper sequencing- and analysis-techniques, the amount of data has exploded. This became increasingly harder and led to the use of computers to analyse. Nowadays, Bio-informatics uses linux-platforms. This has simple but powerful command-line tools that are especially good with the bio-data. But as the data increases, so do the tools to analyse, which are on top of that becoming more and more difficult for laymen, as they require more and more knowledge about the analysis.
Different platforms exist to analyse omics-data. 
    
	bioinformatics not that accessible
As the tools are increasing both in numbers as in complexity, an advanced understanding of these is necessary. However, those that need the tools are mostly not the hardcore statisticians. As a result, handy tools are lost due too complexity or worse incorrectly used.
The Linux platform isn’t that accessible for someone who isn’t used to using it, which makes using tools not handy for those that only need it a few times. This can lead to mistakes with analysis of data, such as incorrect interpretation or incorrect use.

	solution: script with tools
Nextflow is a reactive workflow framework and a programming domain-specific language that eases writing computational pipelines with complex data. In practice a Nextflow pipeline script is made by joining together many different processes. Each process can be written in any scripting language that can be executed by the Linux platform (Bash, Perl, Ruby, Python, etc.). The Nextflow scripting language is an extension of the Groovy programming language whose syntax has been specialized to ease the writing of computational pipelines in a declarative manner. (from nextflow wiki)


## Aim

	summary of the introduction
The boom in big data generation led to the development of bio-informatics; informatics that specializes in analysis of biological-data.
As this 
Develop a tool that enables scientist to analyse and interpret their omics-data with WGCNA, IntCIM, MOFA and MixOmics. The tool is so designed that it utilizes the ideal parameters for the analysis and outputs the combination of the different methods.

## techniques

programming with:

	UNIX

	R

	NEXTFLOW


## Materials and Methods
 

## Nextflow

### Nextflow - the language

Nextflow is developed by the Comparative Bioinformatics group at the Barcelona Center for Genomic Regulation (CRG). It is open source software distributed under the GPL3 licence. (from nextflow.io)

### Pipelines
In computing, a pipeline, also known as a data pipeline,[1] is a set of data processing elements connected in series, where the output of one element is the input of the next one. The elements of a pipeline are often executed in parallel or in time-sliced fashion. Some amount of buffer storage is often inserted between elements. (from wikipedia)
Nf-core – the project


The nf-core project came about at the start of 2018 as the pet-project of Phil Ewels (@ewels). He's the head of the development facility at NGI Stockholm (National Genomics Infrastructure), part of SciLifeLab in Sweden.

The NGI has been developing analysis pipelines for use with it's genomics data for several years and started using a set of standards for each pipeline created. This helped other people run the pipelines on their own systems - typically Swedish research groups at first, but later on other core genomics facilities too.

As the number of people interested in these common pipelines grew, it seemed silly to keep all the pipelines under the umbrella of just SciLifeLab, complete with NGI prefixes and logos. To try to open up the effort into a truly collaborative project, nf-core was created and all relevant pipelines moved to this new GitHub Organisation.
Nf-core installation
pip install --upgrade setuptools
sudo apt-get install python3.6-dev libmysqlclient-dev
 pip install nf-core
 
> one red line: cookiecutter 1.6.0 has requirement requests>=2.18.0, but you'll have requests 2.12.4 which is incompatible.
>> endline: Successfully installed GitPython-2.1.11 arrow-0.12.1 backports.functools-lru-cache-1.5 binaryornot-0.4.4 chardet-3.0.4 cookiecutter-1.6.0 future-0.16.0 gitdb2-2.0.4 jinja2-time-0.2.0 nf-core-1.2 poyo-0.4.2 requests-cache-0.4.13 smmap2-2.0.4 tabulate-0.8.2 whichcraft-0.5.2


## MOFA: Multi-Omics Factor Analysis

MOFA is a factor analysis model that provides a general framework for the integration of multi-omic data sets in a completely unsupervised fashion.
Intuitively, MOFA can be viewed as a versatile and statistically rigorous generalization of principal component analysis (PCA) to multi-omics data. Given several data matrices with measurements of multiple ‘omics data types on the same or on overlapping sets of samples, MOFA infers an interpretable low-dimensional data representation in terms of (hidden) factors. These learnt factors represent the driving sources of variation across data modalities, thus facilitating the identification of cellular states or disease subgroups.

Once trained, the model output can be used for a range of downstream analyses, including the visualisation of samples in factor space, the automatic annotation of factors using (gene set) enrichment analysis, the identification of outliers (e.g. due to sample swaps) and the imputation of missing values. (copy paste)

### Putting MOFA in nextflow

When putting MOFA in nextflow, it is important to addapt the script for compatibility. One of the things is to add a “\” before the “$” of the in script variables.
xkhvsd
## Technical procedures

## Results

## Discussion

## References

## Resources
Installing nextflow on windows 10: https://cipher.readthedocs.io/en/latest/installation.html
Nextflow tutorial: https://www.nextflow.io/docs/latest/getstarted.html
Add folder to cd: https://superuser.com/questions/167221/can-i-add-a-shortcut-to-replace-a-path-in-linux
Installing docker: https://docs.docker.com/install/linux/docker-ce/ubuntu/#install-docker-ce
https://blog.jayway.com/2017/04/19/running-docker-on-bash-on-windows/
