# Capstone Draft 1

## Overview
This project is the first draft of my Capstone project. Here I examine the EEG components of patients and build predict models to classify a patient with a diagnosis. 

## Dataset
This dataset contains the EEG resting state-closed eyes recordings from 88 subjects in total.  
1. Participants: 36 of them were diagnosed with Alzheimer's disease (AD group), 23 were diagnosed with Frontotemporal Dementia (FTD group) and 29 were healthy subjects (CN group). Cognitive and neuropsychological state was evaluated by the international Mini-Mental State Examination (MMSE). MMSE score ranges from 0 to 30, with lower MMSE indicating more severe cognitive decline. The duration of the disease was measured in months and the median value was 25 with IQR range (Q1-Q3) being 24 - 28.5 months. Concerning the AD groups, no dementia-related comorbidities have been reported. 
2. Recordings: Recordings were aquired with 19 scalp electrodes (Fp1, Fp2, F7, F3, Fz, F4, F8, T3, C3, Cz, C4, T4, T5, P3, Pz, P4, T6, O1, and O2) according to the 10-20 international system and 2 reference electrodes (A1 and A2) placed on the mastoids for impendance check, according to the manual of the device. Each recording was performed according to the clinical protocol with participants being in a sitting position having their eyes closed. 
3. Preprocessing: First, a Butterworth band-pass filter 0.5-45 Hz was applied and the signals were re-referenced to A1-A2. 
Then, the Artifact Subspace Reconstruction routine (ASR) which is an EEG artifact correction method included in the EEGLab Matlab software was applied to the signals, 
removing bad data periods which exceeded the max acceptable 0.5 second window standard deviation of 17, which is considered a conservative window. 
Next, the Independent Component Analysis (ICA) method (RunICA algorithm) was performed, transforming the 19 EEG signals to 19 ICA components. 
https://openneuro.org/datasets/ds004504/versions/1.0.2

## Research Question: 
### 1. Can the analysis of specific EEG components, such the power spectrum, be used as reliable biomarkers to predict the diagnosis of Alzheimer's disease?

Aim: To investigate the potential relationship between the power spectrum and Alzheimer's disease diagnosis.

Importance: the importance of this research question lies in the potential for advancing early detection, diagnosis, and understanding of Alzheimer's disease by exploring the role of specific EEG components, such as the power spectrum, as reliable biomarkers.
Currently, diagnosing Alzheimer's disease relies on a combination of clinical assessments, cognitive tests, and neuroimaging techniques. 
However, having reliable biomarkers that can accurately predict the diagnosis of Alzheimer's disease would greatly enhance early detection and intervention strategies.
By exploring the analysis of specific EEG components, particularly the the power spectrum, as potential biomarkers, this research question addresses the need for non-invasive and accessible diagnostic tools. 
If specific EEG components, such as the power spectrum, are found to be reliably associated with Alzheimer's disease diagnosis, it could provide a simpler and more cost-effective method for identifying individuals at risk or in the early stages of the disease.
Furthermore, understanding the relationship between the power spectrum and Alzheimer's disease diagnosis can contribute to our knowledge of the underlying neurophysiological changes associated with the disease. 

Analysis: Classification model pipelines for multi class classification

### 2. What specific independent component analysis (ICA) derived EEG components are significantly predictive of cognitive decline and impairment in adults with dementia?

Aim: To identify EEG components that can serve as predictive markers for cognitive decline and impairment

Importance: Cognitive decline and impairment are central features of dementia, and identifying specific EEG components that are significantly predictive of these outcomes can have several important implications.
Firstly, the identification of EEG components that are associated with cognitive decline in dementia can provide valuable insights into the underlying neural mechanisms and brain changes that occur as cognitive impairment progresses.
Secondly, discovering EEG components that serve as predictive markers for cognitive decline and impairment has the potential to improve the early detection and diagnosis of dementia. 
Furthermore, by identifying specific EEG components that are predictive of cognitive decline, healthcare professionals may be able to tailor interventions and therapies to target the affected brain regions or networks, leading to more effective and targeted treatment approaches.

Analysis: Regression model pipelines for numerical predictions.

## Dataset and Notebook
The link to the dataset is:
The link to the Jupyter Notebook is:

## Initial Data Findings
1. Chose the decision tree classification model as it provided the highest accuracy scores and it is an easy model to interpret.
2. Accuracy of determining the control group: , frontotemporal dementia: , Alzheimers: .

## Business Findings
EEG components can be used as a cost effective, non-intrusive method to diagnose dementia. 

More accuracte predictions can be made once more data is collected.

## Next Steps
1. Remove warnings
2. Refine and interpret Results
3. Translate interpreted results in non-technical terms
4. Answer second research question using regression models