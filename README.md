# Machine learning approach for prediction of COVID-19 infection and classification of SARS-CoV-2 variants

### Team Members
1. Mike Mwanga
2. Evans Mudibo
3. Hesbon Omwondho

Background
The emergence and rapid spread of coronavirus disease 2019 (COVID-19) caused by severe acute respiratory syndrome coronavirus 2 (SARS-CoV-2) as a potentially fatal disease is a major and urgent threat to global health. COVID-19 is transmitted through direct contact with an infected person via sneezing and coughing and has no medically approved vaccine or medication[1], [2]. Upon infection, patients exhibit several significant symptoms including fever, cough, diarrhea which are more severe in adults with chronic illness, and shortness of breath[2]. The existence of asymptomatic cases and lack of diagnostic kits have resulted in delayed or even missed-diagnosis, exposing patients, visitors and healthcare workers to SARS-CoV-2 infection, posing a great challenge to the healthcare and economic sectors. 
Currently, PCR and sequencing methods have been deployed to identify and classify SARS-CoV-2 variants[3]. However, the design of primers and probes limits these methods to identify only known variants and require continuous update to cater for new species or strains that are clinically relevant.  High-throughput sequencing provides an unbiased identification of virus molecules present in samples and can be used for systematic classification of SARS-CoV-2 variants. However, this approach requires large scaled reference databases of variants to compare against resulting to considerable computing requirements. 
Non-clinical techniques such as machine learning (ML), and other artificial intelligence techniques can be implemented in diagnosis, classification and eventually control of COVID-19[4], [5]. ML based tools can identify and extract the important sequence features for sequence classification in a computationally efficient manner. Such have been successfully used previously in solving sequence classification problems[5]. Despite these advances, none has been applied in classifying SARS-CoV-2 variants. Accurate and timely diagnostic of COVID-19 and classification of SARS-CoV-2 variants will eventually reduce the huge burden on the limited health system while providing efficient and diagnostic and predictable methods for SARS-CoV-2.
Machine learning (ML) is one of the most advanced AI techniques which has shown potential for diagnosing, containing and therapeutic monitoring of many diseases. In this work we intend to employ machine learning techniques on publicly available epidemiological and genomics dataset to predict infection by SARS-CoV-2 and classify variants. 


Aims and Objectives
1.	To develop machine learning model for predicting which patients are infected with SARS-CoV-2.
2.	To classify SARS-CoV-2 variants using genomic sequence data and machine learning

Significance of Study
COVID-19 has brought with its immense burden to the healthcare system globally. Currently, vaccination is the only available control measure for control and spread of COVID-19, thus early identification of patients may facilitate provision of immediate and proper treatment in advance and reduce mortality. Implementing ML approach will serve to augment human diagnostic performance and show great potential and assist in management of COVID-19. Accurate classification will enable effective monitoring and tracking of SARS-CoV-2 variants and improve in control and management of the pandemic. 

Methods and workflow
This project will make use of publicly available dataset of positive and negative COVID-19 cases from Mexico. Details about the dataset can be found here link. Figure 1 shoes workflow for data preparation and model implementation to predict COVID-19 infections on epidemiological data. 

For classification of SARS-CoV-2, representative genomic sequences data for the spike protein of all SARS-CoV-2 variants will be downloaded from GISAID and GenBank databases. Sequence clean-up and analysis will be performed using publicly available bioinformatics tools such as AliView. Machine learning algorithms will be implemented using python packages and libraries such as pandas, SciPy, scikit, and TensorFlow. The data will be cleaned and labeled followed by feature extraction for ML predictions. Features extraction from genomic sequence data for machine learning purpose will be done using relative synonymous codon usage (RSCU) approach[6]. This approach makes use of the fact that proteins are made up of 20 amino acids which are coded by 64 codons. Since trinucleotide coding for the same amino acid are not random, some species prefer one codon over the other. RSCU values will be calculated by determined as the ratio of the observed number of codon occurrence to expected usage assuming uniform distribution[6]. This dataset will be split into training and testing for selection of appropriate ML models, which will in turn be used classifying the variants.

