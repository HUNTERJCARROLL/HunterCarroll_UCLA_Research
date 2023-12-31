University of California Los Angeles Bruins In Genomics Summer Research - Hunter Carroll

https://qcb.ucla.edu/big-summer/big2023/#toggle-id-9 

PI : Chongyuan Luo

Direct Mentor : Matthew Heffel

---

Abstract: 

Gaussian Mixture Variational Autoencoder for Imputation and Batch Correction of DNA Methylation Data

HUNTER CARROLL1,2, Matthew Heffel3,4, Cuining Liu3, Chongyuan Luo3

1 BIG Summer Program, Institute for Quantitative and Computational Biosciences, UCLA

2 University of Colorado, Denver

3 Department of Human Genetics David Geffen School of Medicine, UCLA

4 Bioinformatics Interdepartmental Program, UCLA

Cytosine methylation (mC) is a crucial epigenetic modification regulating gene expression and cellular development. However, mC suffers from high dimensionality when studying multiple CpG sites astride the genome. When analyzing collective age groups of the prefrontal cortex our data suffers from interpolated sources of variation between the high-variance and low-variance features. To model cellular development between sources of variation, like age, we have investigated the use of neural networks as a remedy for information loss. Additionally, using a Gaussian Mixture (GM) model in the latent space of a variational autoencoder may serve to improve clustering, batch effect correction, and imputation by providing non-discrete variational autoencoder latent space parameters. We examine the use of GM Models in the latent space on the adult prefrontal cortex to showcase validity and set the stage for expanding our method to sizable datasets composed of multiple tissues and ages.


---

Abstract Points:

Cytosine methylation (mC) is a crucial epigenetic modification regulating gene expression and cellular development. However, mC suffers from high dimensionality when studying multiple CpG sites astride the genome. Using the gene body counts from the adult prefrontal cortex we aim to reduce the in-group (cell-type) variation by using neural networks.Our data: single-nucleus methyl-3C sequencing (sn-m3C-seq) to capture chromatin organization and DNA methylation informationWe use three neural network models that are the Autoencoder (AE), variational Autoencoder (VAE), and a Gaussian Mixed VAE to interpret the adult prefrontal cortex in terms of in-group variance, reconstructive capabilities, and clustering. Our high-variance genes are determined by ranking gene groups and identifying n-chosen differentially expressed marker genes from each cell-type group. 

---

Notes for Improvement:

Priority Number One: UMAP is not always a meaningful method for determining biologically relevant information for it tends to distort the original manifold.UMAP suffers from noise and outliers, parameter sensitivity, and most importantly the balance tradeoff between local and global features. As shown in the analysis our models perform modestly on the high-variance features but when it comes to the low-variance features our methods suffer from extremely high dimensionality and sparse data density. Our goal is to be able to take advantage of neural networks as a means to preserve global features displayed by high-variance features and use them to condition the low-variance features to limit the distortion exhibited by other dimensionality reduction techniques. 
Priority Number Two: Validating batch correction via marker gene expression and imputation accuracy. 
Priority Number Three: Determining highly variable features and lowly variable features plays a substantial role in the performance of our models. For further analysis, we would work towards using different thresholds and methods for determining our high variance features.

---

Conclusions: 

Our models demonstrate the reduction of noise within individual cell types and the accuracy of reconstruction by measuring the unsupervised Leiden cluster assignments between the input and reconstructed data.
We focus on the adult prefrontal cortex using 456 highly variable genes determined via differential expression in ranked gene groups. Our models demonstrate modest performance in terms of both our data reconstruction and clustering capabilities. 
A noteworthy observation is that our Autoencoder performs best at noise reduction but our Gaussian Mixed Variational Autoencoder performs best in terms of clustering accuracy demonstrating an important trade-off to be considered for further analysis. 
Our goal is to develop a model that can successfully balance these two objectives by creating a branched Gaussian Mixed VAE that employs the high variance genes to drive the reconstruction and clustering accuracy of the low variance genes by assigning Gaussian membership probabilities in our latent spaces as shown in the figure to the right. 
