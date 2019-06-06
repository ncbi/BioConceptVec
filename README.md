# BioConceptVec: <br><small>creating and evaluating literature-based biomedical concept embeddings on a large scale</small>


## Table of contents

* [Text corpora](#text-corpora)
* [Named Entity Recognition (NER) tools](#pubtator)
* [BioConceptVec: embeddings and concept files](#bioconceptvec)
* [Tutorial](#tutorial)
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
You can find [this tutorial](https://github.com/ncbi-nlp/BioSentVec/blob/master/BioSentVec_tutorial.ipynb) on how to use BioConceptVec (for both embedding and concept-only files) for a quick start.


## Acknowledgments
<a name="acknowledgments"></a>
This work was supported by the Intramural Research Programs of the National Institutes of Health, National Library of Medicine. 
