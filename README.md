# Machine learning approach for prediction of COVID-19 infection and classification of SARS-CoV-2 variants

### Team Members
1. Mike Mwanga
2. Evans Mudibo
3. Hesborn Omwanndho
4. Olaitan Awe

## Background <br>
The emergence and rapid spread of coronavirus disease 2019 (COVID-19) caused by severe acute respiratory syndrome coronavirus 2 (SARS-CoV-2) as a potentially fatal disease is a major and urgent threat to global health. COVID-19 is transmitted through direct contact with an infected person via sneezing and coughing and has no medically approved vaccine or medication[1], [2]. Upon infection, patients exhibit several significant symptoms including fever, cough, diarrhea which are more severe in adults with chronic illness, and shortness of breath[2]. The existence of asymptomatic cases and lack of diagnostic kits have resulted in delayed or even missed-diagnosis, exposing patients, visitors and healthcare workers to SARS-CoV-2 infection, posing a great challenge to the healthcare and economic sectors. 
Currently, PCR and sequencing methods have been deployed to identify and classify SARS-CoV-2 variants[3]. However, the design of primers and probes limits these methods to identify only known variants and require continuous update to cater for new species or strains that are clinically relevant.  High-throughput sequencing provides an unbiased identification of virus molecules present in samples and can be used for systematic classification of SARS-CoV-2 variants. However, this approach requires large scaled reference databases of variants to compare against resulting to considerable computing requirements. 
Non-clinical techniques such as machine learning (ML), and other artificial intelligence techniques can be implemented in diagnosis, classification and eventually control of COVID-19[4], [5]. ML based tools can identify and extract the important sequence features for sequence classification in a computationally efficient manner. Such have been successfully used previously in solving sequence classification problems[5]. Despite these advances, none has been applied in classifying SARS-CoV-2 variants. Accurate and timely diagnostic of COVID-19 and classification of SARS-CoV-2 variants will eventually reduce the huge burden on the limited health system while providing efficient and diagnostic and predictable methods for SARS-CoV-2.
Machine learning (ML) is one of the most advanced AI techniques which has shown potential for diagnosing, containing and therapeutic monitoring of many diseases. In this work we intend to employ machine learning techniques on publicly available epidemiological and genomics dataset to predict infection by SARS-CoV-2 and classify variants. 


## Aims and Objectives <br>
1.	To develop machine learning model for predicting which patients are infected with SARS-CoV-2.
2.	To classify SARS-CoV-2 variants using genomic sequence data and machine learning

## Significance of Study <br>
COVID-19 has brought with its immense burden to the healthcare system globally. Currently, vaccination is the only available control measure for control and spread of COVID-19, thus early identification of patients may facilitate provision of immediate and proper treatment in advance and reduce mortality. Implementing ML approach will serve to augment human diagnostic performance and show great potential and assist in management of COVID-19. Accurate classification will enable effective monitoring and tracking of SARS-CoV-2 variants and improve in control and management of the pandemic. 

## Methods
### Dataset
Classification of SARS-Cov-2 variants will make use of publicly available representative spike-protein sequence data downloaded from the GISADI and/or GenBank Databases.

### Data processing
ML algorithms do make use of numerical data and since DNA sequences are in categorical form, some form of conversion using readly available tools will be implemented. In this study, label encoding and k-mer encoding techniques are used to convert the sequence data into numerical form. Seqeuences will first be converted into k-mers (which size will be appropriate, 3? In relation to codons?). This will result to k-mer patterns specific for each variant. The label-encoding process will implement LabelEncoder(), where, each k-mer is assigned a numerical value in a sequential manner. The resulting 2D sequence representation numerical matrix will be binarized using  LabelBinarizer(), figure 1. How do we deal with Ns and ambiguous nucleotides?

![Figure 1](https://github.com/mikemwanga/Application-of-Machine-Learning-in-Genomics/blob/main/images/Figure_2.png)

### Classification model
The resulting dataset is fed into a convolutional neural network model (CNN) for feature   extraction. CNN uses convolutionary layers to automatically extract features from a dataset as opposed to other models which require the user to manually extract important features. CNN contains several layers, one input, several hidden and one output layer and each layer contains several neurons and each neuron contains several parameters (link). 



## References <br>
[1]	H. A. Rothan and S. N. Byrareddy, “The epidemiology and pathogenesis of coronavirus disease (COVID-19) outbreak,” Journal of Autoimmunity, vol. 109. 2020. doi: 10.1016/j.jaut.2020.102433.

[2]	M. A. Shereen, S. Khan, A. Kazmi, N. Bashir, and R. Siddique, “COVID-19 infection: Origin, transmission, and characteristics of human coronaviruses,” Journal of Advanced Research, vol. 24. 2020. doi: 10.1016/j.jare.2020.03.005.

[3]	S. Sethi and T. Chakraborty, “Molecular (real-time reverse transcription polymerase chain reaction) diagnosis of SARS-CoV-2 infections: Complexity and challenges,” Journal of Laboratory Medicine, vol. 45, no. 3. 2021. doi: 10.1515/labmed-2020-0135.

[4]	D. A. Mendels et al., “Using artificial intelligence to improve COVID-19 rapid diagnostic test result interpretation,” Proceedings of the National Academy of Sciences of the United States of America, vol. 118, no. 12, Mar. 2021, doi: 10.1073/pnas.2019893118.

[5]	O. P. Singh, M. Vallejo, I. M. El-Badawy, A. Aysha, J. Madhanagopal, and A. A. Mohd Faudzi, “Classification of SARS-CoV-2 and non-SARS-CoV-2 using machine learning algorithms,” Computers in Biology and Medicine, vol. 136, 2021, doi: 10.1016/j.compbiomed.2021.104650.

[6]	G. S. Randhawa, M. P. M. Soltysiak, H. el Roz, C. P. E. de Souza, K. A. Hill, and L. Kari, “Machine learning using intrinsic genomic signatures for rapid classification of novel pathogens: COVID-19 case study,” PLoS ONE, vol. 15, no. 4, Apr. 2020, doi: 10.1371/journal.pone.0232391.

[7]	Z. Bzhalava, A. Tampuu, P. Bała, R. Vicente, and J. Dillner, “Machine Learning for detection of viral sequences in human metagenomic datasets,” BMC Bioinformatics, vol. 19, no. 1, Sep. 2018, doi: 10.1186/s12859-018-2340-x.

