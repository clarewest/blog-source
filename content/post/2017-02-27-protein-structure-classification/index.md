---
title: "Protein Structure Classification: Order in the Chaos"
author: CE West
date: '2017-02-28'
slug: protein-structure-classification
categories:
  - personal
tags:
  - phd
  - proteins
  - bioinformatics
meta_img: images/image.png
description: Overview of protein structure classification
---

This post gives an overview of systematic approaches for protein structure classification based on sequence and structural similarity, which are essential for understanding protein function and evolution, as well as for training and benchmarking new methods for protein structure prediction. 

<!--more-->

The number of known protein structures has increased exponentially over the past decades; there are currently over 127,000 structures deposited in the PDB[^1]. To bring order to this large volume of data, and to further our understanding of protein function and evolution, these structures are systematically classified according to sequence and structural similarity. Downloadable classification data can be used for annotating datasets, exploring the properties of proteins and for the training and benchmarking of new methods [^2].

<div class="figure">

![Number of structures in the PDB](https://www.blopig.com/blog/wp-content/uploads/2017/02/pdb_structures.png?ssl=1)

<p class="caption">Yearly growth of structures in the PDB (adapted from [^1]</p>

</div>

Typically, proteins are grouped by structural similarity and organised using hierarchical clustering. Proteins are sorted into classes based on overall secondary structure composition, and grouped into related families and superfamilies. Although this process could originally be manually curated, as with Structural Classification of Proteins ([SCOP](http://scop.mrc-lmb.cam.ac.uk/scop/)) [^3] (last updated in June 2009), the growing number of protein structures now requires semi- or fully-automated methods, such as SCOP-extended ([SCOPe](http://scop.berkeley.edu/)) [^4] and Class, Architecture, Topology, Homology ([CATH](http://www.cathdb.info/)) [^5]. These resources are comprehensive and widely used, particularly in computational protein research. There is a large proportion of agreement between these databases, but subjectivity of protein classification is to be expected. Variation in methods and hierarchical structure result in differences in classifications.  For example, different criteria for defining and classifying domains results in inconsistencies between CATH and SCOPe.

The arrangements of secondary structure elements in space are known as folds. As a result of evolution, the number of folds that exist in nature is thought to be finite, predicted to be between 1000-10,000 [^6]. Analysis of currently known structures appears to support this hypothesis, although solved structures in the PDB are likely to be a skewed sample of all protein structures space. Some folds are extremely commonly observed in protein structures.

In his ‘periodic table for protein structures’, William Taylor went one step further in his goal to find a comprehensive, non-hierarchical method of protein classification [^7]. He attempted to identify a minimal set of building blocks, referred to as basic Forms, that can be used to assemble as many globular protein structures as possible. These basic Forms can be combined systematically in layers in a way analogous to the combination of electrons into valence shells to form the periodic table. An individual protein structure can then be described as the closest matching combination of these basic Forms.  Related proteins can be identified by the largest combination of basic Forms they have in common.

<div class="figure">

![Basic forms diagram](https://www.blopig.com/blog/wp-content/uploads/2017/02/TaylorForms.jpg?w=600&ssl=1)

<p class="caption">The ‘basic Forms’ that make up Taylor’s ‘periodic table of proteins’. These secondary structure elements accounted for, on average, 80% of each protein in a set of 2,230 structures (all-alpha proteins were excluded from the dataset) [^7]</p>

</div>

The classification of proteins by sequence, secondary and tertiary structure is extensive. A relatively new frontier for protein classification is the quaternary structure: how proteins assemble into di-, tri- and multimeric complexes. In a recent publication by an interdisciplinary team of researchers, an analysis of multimeric protein structures in combination with mass spectrometry data was used to create a ‘periodic table of protein complexes’ [^8]. Three main types of assembly steps were identified: dimerisation, cyclisation and heteromeric subunit addition. These types are systematically combined to predict many possible topologies of protein complexes, within which the majority of known complexes were found to reside. As has been the case with tertiary structure, this classification and exploration of of quaternary structure space could lead to a better understanding of protein structure, function and evolutionary relationships. In addition, it may inform the modelling and docking of multimeric proteins.

*This blog post was originally posted on the [OPIG blog](https://www.blopig.com/blog/2017/02/protein-structure-classification-order-in-the-chaos/).*

![]()

[^1]: [RCSB PDB Statistics](http://www.rcsb.org/pdb/static.do?p=general_information/pdb_statistics/index.html)

[^2]: Fox, N.K., Brenner, S.E., Chandonia, J.-M., 2015. The value of protein structure classification information-Surveying the scientific literature. Proteins Struct. Funct. Bioinforma. 83, 2025–2038.

[^3]: Murzin AG, Brenner SE, Hubbard T, Chothia C., 1995. SCOP: a structural classification of proteins database for the investigation of sequences and structures. J Mol Biol. 247, 536–540.

[^4]: Fox, N.K., Brenner, S.E., Chandonia, J.-M., 2014. SCOPe: Structural Classification of Proteins–extended, integrating SCOP and ASTRAL data and classification of new structures. Nucleic Acids Res. 42, 304-9.

[^5]: Dawson NL, Lewis TE, Das S, et al., 2017. CATH: an expanded resource to predict protein function through structure and sequence. Nucleic Acids Research. 45, 289-295.

[^6]: Derek N Woolfson, Gail J Bartlett, Antony J Burton, Jack W Heal, Ai Niitsu, Andrew R Thomson, Christopher W Wood,. 2015. De novo protein design: how do we expand into the universe of possible protein structures?, Current Opinion in Structural Biology, 33, 16-26.

[^7]: Taylor, W.R., 2002. A “periodic table” for protein structures. Nature. 416, 657–660.

[^8]: Ahnert, S.E., Marsh, J.A., Hernandez, H., Robinson, C. V., Teichmann, S.A., 2015. Principles of assembly reveal a periodic table of protein complexes. Science. 80, 350




