# BioConceptVec: <br><small>creating and evaluating literature-based biomedical concept embeddings on a large scale</small>


## Table of contents

* [Text corpora](#text-corpora)
* [Named Entity Recognition (NER) tools](#pubtator)
* [BioConceptVec: embeddings and concept files](#bioconceptvec)
* [Tutorial](#tutorial)
* [Datasets](#dataset)
* [Acknowledgments](#acknowledgments)


## Text corpora
<a name="text-corpora"></a>
We created BioConceptVec using the entire [PubMed](https://www.ncbi.nlm.nih.gov/pubmed/). The texts were split and tokenized using [NLTK](https://www.nltk.org/). We also lowercased all the words.


## Using PubTator for annotating concepts in the PubMed
<a name="pubtator"></a>
We employed [PubTator](https://www.ncbi.nlm.nih.gov/research/pubtator/) to annotate biomedical concepts in the PubMed. It covers genes, mutations, chemicals, diseases and cellines. The trained embeddings contain over 400,000 concepts.

## BioConceptVec: embeddings and concept files
<a name="bioconceptvec"></a>
We release four versions of BioConceptVec (cbow, skip-gram, glove and fastText). For each version, we make both the **embedding**(contains concepts and other words) in binary format and the **concept-only** file in json format available.

1. **BioConceptVec cbow:** [embedding](https://ftp.ncbi.nlm.nih.gov/pub/lu/BioConceptVec/bioconceptvec_word2vec_cbow.bin) (2.4GB) and [concept-only](https://ftp.ncbi.nlm.nih.gov/pub/lu/BioConceptVec/concept_cbow.json) (798MB).
2. **BioConceptVec skip-gram:** [embedding](https://ftp.ncbi.nlm.nih.gov/pub/lu/BioConceptVec/bioconceptvec_word2vec_skipgram.bin) (2.4GB) and [concept-only](https://ftp.ncbi.nlm.nih.gov/pub/lu/BioConceptVec/concept_skip.json) (812MB).
3. **BioConceptVec glove:** [embedding](https://ftp.ncbi.nlm.nih.gov/pub/lu/BioConceptVec/bioconceptvec_glove.bin) (2.4GB) and [concept-only](https://ftp.ncbi.nlm.nih.gov/pub/lu/BioConceptVec/concept_glove.json) (835MB).
4. **BioConceptVec fastText:** [embedding](https://ftp.ncbi.nlm.nih.gov/pub/lu/BioConceptVec/bioconceptvec_fasttext.bin) (2.4GB) and [concept-only](https://ftp.ncbi.nlm.nih.gov/pub/lu/BioConceptVec/concept_fast.json) (813MB).


## Tutorial
<a name="pubtator"></a>
You can find [this tutorial](https://github.com/ncbi-nlp/BioConceptVec/blob/master/bioconcept_tutorial.ipynb) on how to use BioConceptVec (for both embedding and concept-only files) for a quick start.

## Datasets
<a name="dataset"></a>
We also make all the 9 evaluation datasets publicly available. It covers 4 applications:

1. [**Drug-Gene interactions**](https://github.com/ncbi-nlp/BioConceptVec/tree/master/datasets/drug_gene_interactions). A tsv file contains (1) ID: the instance ID, (2) num_of_genes: the number of genes for this instance, (3) pos_rel_genes: the IDs of related genes, and (4) neg_rel_genes: the IDs of unrelated genes.

2. [**Gene-Gene interactions**](https://github.com/ncbi-nlp/BioConceptVec/tree/master/datasets/gene_gene_interactions). 5 datasets on gene-gene interactions that have same format as above.

3. [**Protein-Protein interaction**](https://github.com/ncbi-nlp/BioConceptVec/tree/master/datasets/protein_protein_interactions). It contains two datasets: (1) combined: protein-protein interactions created based on STRING combined scores and (2) exp700: protein-protein interactions created based on STRING experimental scores over 700. Both datasets contain train, valid and test files. The file contains (1) query: query protein ID, (2) subject: subject protein ID, (3) score: STRING score and (4) label: whether it is a protein-protein interaction.

4. [**Drug-Drug interaction**](https://github.com/ncbi-nlp/BioConceptVec/tree/master/datasets/drug_drug_interactions). This dataset is from [Drug-Drug interaction semeval-2013](https://www.cs.york.ac.uk/semeval-2013/task9/). Please see the details there.

## Acknowledgments
<a name="acknowledgments"></a>
This work was supported by the Intramural Research Programs of the National Institutes of Health, National Library of Medicine. 
