# MTCNN Reproduction - COMP3314 Group Project

## Overview
This project reproduces the **MTCNN (Multi-task Cascaded Convolutional Networks)** framework for joint face detection and facial landmark localization, as proposed by Zhang et al. (2016). The implementation is fully re-written in PyTorch (the original paper used TensorFlow).

## My Role & Contributions (Tang Linchuan)
As a core member of the 4-person group, I contributed to:
- Implementation of the **P-Net, R-Net, and O-Net** architectures.
- Resolving **dimensional mismatches** between cascaded networks by designing a dynamic data-flow pipeline.
- Optimizing inference speed by refactoring the pipeline to eliminate costly **NumPy-Tensor conversions** (achieved ~30% runtime improvement).
- Drafting key sections of the final report, including implementation details, experimental results, and error analysis.

## Key Results
Evaluated on the FDDB benchmark, our reproduction achieved:
- **Precision**: 95.25%
- **Recall**: 88.36%
- **F1-Score**: 91.68%
- **PR-AUC**: 0.90
- **ROC-AUC**: 0.92

These results are competitive with the original paper, with the minor performance gap attributed to the absence of online hard sample mining (OHSM) and limited training data scale.

## Technical Stack
- **Framework**: PyTorch
- **Languages**: Python
- **Key Techniques**: CNN, Multi-task Learning, Non-Maximum Suppression (NMS), Image Pyramid

## Report
The full project report with detailed methodology, data preprocessing steps, and result analysis is available here:  
**[COMP3314_MTCNN_Reproduction_Report.pdf](./COMP3314_MTCNN_Reproduction_Report.pdf)**

## Source Code
The complete source code for this project is maintained in our group's original repository:  
**[https://github.com/Catherine135/MTCNN_Pytorch_Reproduction](https://github.com/Catherine135/MTCNN_Pytorch_Reproduction)**

> *Note: This repository serves as a documentation archive and personal portfolio record. All source code rights are shared among group members.*
