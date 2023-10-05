# GENER: A Parallel Layer Deep Learning Network To Detect Gene-Gene Interactions From Gene Expression Data
A tensorflow implementation of our parallel deep learning network mentioned in our paper.

## Architecture of GNE
![Architecture of GNE](https://github.com/AhmedFakhry47/GENER/blob/main/Plots/gener-model-plot.png)

Our deep learning (DL) model is an ensemble learning architecture with two parallel branches (Figure 1), leveraging both convolutional neural networks (CNNs) and multi-layer feedforward neural networks (MFNNs). Specifically, we utilize CNNs to discern patterns and correlations among gene pairs within a vast dataset. Conversely, the MFNN takes as input the dot product of two gene expression vectors for each gene pair. Our network is trained through late fusion, where we combine the high-level features extracted from these two parallel branches.

Requirements 
* TensorFlow 2.0
* python3.6 or more
* sklearn
* itertools
* scipy
* numpy
  

## Data

for training our parallel layer deep learning network, we have used gene expression data alongside gene-gene interaction information from multiple data sources. To ensure the robustness of our approach, we conducted two separate training trials on each of these datasets separately. Additionally, in section 4, we compared the findings of our deep learning network to GNE and other other deep learning and statistical models, with the results obtained from the second training experiment. For the second training experiment, DREAM5 and BioGRID datasources have been utilized. The BioGRID& DREAM5 combined dataset consists of 5950 unique gene expressions and 977481 GGI pairs available for training and testing. Meanwhile, for our first training experiment, we have used gene expression and gene-gene interaction information offered by Yeastract DataBase, which included 5970 unique gene expressions and 6736 GGI pairs. For the gene expressions obtained from the Yeastract DataBase, each data point comprised a vector of 1012 floating-point values. On the other hand, the gene expressions' length for the DREAM5&BioGRID combined dataset was 536. 

References and information about these datasources could be found in

| Dataset        | Source           | 
| ------------- |:-------------:|
| Interaction dataset  | [BioGRID](http://thebiogrid.org/) | 
| Gene expression data     | [DREAM5 Challenge](http://dreamchallenges.org/project/dream-5-network-inference-challenge/)    |  
| Gene expression & interaction data | [YEASTRACT](http://www.yeastract.com) |  


## Settings

* For the first training experiment, you can check "RGN_GUI_V4.ipynb"
* For the second training experiment, you can check the model weights and the data folder in addition to the "gener script.ipynb"


## Model Results
![GENER Results](https://github.com/AhmedFakhry47/GENER/blob/main/Plots/Model%20Results.png)

## Contact
ahmedfakhry@knu.ac.kr

