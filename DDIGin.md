## DDIG in

Method: **SVM** + training on HGMD (disease causing) and 1000GP(neutral)

    we found that the most discriminative feature for FS indels and NS variants was the **disruption of DNA conservation**, **rather than the disruption of protein structure** as in the case of NFS indels

    We evaluated 36 different features 

    We used the sequential forward floating selection (SFFS) algorithm (Pudil etal., 1994) to find an effective combination of features which we used for training the final SVM model


## Features

### Global features

- Ka/Ks ratio
    + We downloaded pre-calculated Ka and Ks values for the human-chimpanzee, human-macaque, human-mouse and human-rat alignments from Ensembl (release 75) (Flicek etal., 2013) and calculated the average Ka/Ks ratio for the four alignments.
- number of transcripts
    + ?
- We also examined nine global transcript-level features (calculated as the average, minimum or maximum of all transcripts of the given gene): 
    1 number of exons; 
    2 relative exon number; 
    34 distance to the nearest upstream (downstream) splice site; 
    567 relative distance to the5′end, 3′end and centre of the sequence;
    8 relative length of the variant; 
    9 and relative length of the mutated sequence

### local features

- DNA conservation
    +  The DNA conservation was derived from phylogenetic P-values of the multiple alignments of 45 vertebrates to the human genome calculated with the phyloP program
- PSSM
    + feature PSSM conservation
- protein conservation scores 
    + Shannon entropy
    + hhBLITS
- 5 protein structural features
    + rasa
    + helix sheet coil and disorder probabilities
