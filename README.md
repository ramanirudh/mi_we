# METEOR_Indic_WE
Indic Meteor with Word-embeddings.

This version has been created by modifying the following two versions of Meteor:
1. METEOR-E which is an enhanced version of the METEOR metric v1.5 using DBnary and Word Embeddings (https://github.com/cservan/METEOR-E)
2. METEOR-Indic (https://github.com/anoopkunchukuttan/meteor_indic) which has synonymy modules from Indic Word-net.

## How to use Embeddings data

First, learn Word Embeddings using using word embeddings toolkit like multivec (https://github.com/eske/multivec) and save the model in text format.
then, you can activate the module called "embeddings" (with the switch "m") and specify the embeddings model with the switch "emb". The decision threshold for deciding whether an alignment is possible is set to 0.8, but you can set another one with the switch "embTh". 

Here is an example:

        java -jar meteor-1.4.jar test reference -l en -m 'exact stem synonym embeddings ' -emb ./resources/word-embeddings/embeddings.en -embTh 0.85
        
For our work, we have used pre-trained word embeddings from the paper entitled '"A Passage to India": Pre-trained Word Embeddings for Indian Languages' (https://www.cfilt.iitb.ac.in/~diptesh/embeddings/). 

If you use this code, please cite the following work:

https://link.springer.com/chapter/10.1007/978-981-16-6624-7_3

@InProceedings{10.1007/978-981-16-6624-7_3,
author="Anirudh, Ch Ram
and Murthy, Kavi Narayana",
editor="Satapathy, Suresh Chandra
and Peer, Peter
and Tang, Jinshan
and Bhateja, Vikrant
and Ghosh, Anumoy",
title="Machine Translation System Combination with Enhanced Alignments Using Word Embeddings",
booktitle="Intelligent Data Engineering and Analytics",
year="2022",
publisher="Springer Nature Singapore",
address="Singapore",
pages="19--29",
isbn="978-981-16-6624-7"
}
