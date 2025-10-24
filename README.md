# Radiomic clustering using graph network techniques coupled with unbalanced optimal transport 

![UOTK](img/Data_analysis_pipeline.png)
Radiogenomic data analysis pipeline. Sample clustering was conducted using our proposed network-based k-means method coupled with unbalanced optimal transport on radiomic features to identify sub-groups. Tumor immune cell abundance was then compared between the identified sub-groups.


![UOTK](img/Unbalanced_OMT.png)
Introduction of unbalanced optimal transport. (A) The cost and transport plan matrices (C ̃ and T ̃) for unbalanced optimal transport and (B) A displacement interpolation on a network between two samples (S1 and S2). Unbalanced optimal transport allows for injection and extraction of mass to and from the network.


1. Model Building  
   - PathCNN.py  

2. GradCAM  
   - PathCNN_GradCAM_modeling.py: to generate a model for GradCAM (PathCNN_model.h5)
   - PathCNN_GradCAM.py: to generate GradCAM images and a resultant file (pathcnn_gradcam.csv)

3. Multi-omics data
   - GBM multi-omics data including mRNA expression, CNV, and DNA methylation were downloaded from the CBioPortal database.
   - Pathway information was downloaded from the KEGG database.
   - PCA was performed for each pathway in individual omics types.
   
   Five PCs in each omics type are in the following files:
   - PCA_EXP.xlsx, PCA_CNV.xlsx, PCA_MT.xlsx
   
   Clinival variables are in the following file:
   - Clinical.xlsx
