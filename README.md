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
        
For our work, we have used pre-trained word embeddings from the paper titled "A Passage to India": Pre-trained Word Embeddings for Indian Languages (https://aclanthology.org/2020.sltu-1.49/) 

If you use this code, please cite the following work:

Anirudh, C.R., Murthy, K.N. (2022). Machine Translation System Combination with Enhanced Alignments Using Word Embeddings. In: Satapathy, S.C., Peer, P., Tang, J., Bhateja, V., Ghosh, A. (eds) Intelligent Data Engineering and Analytics. Smart Innovation, Systems and Technologies, vol 266. Springer, Singapore. https://doi.org/10.1007/978-981-16-6624-7_3
