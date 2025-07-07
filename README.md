A Explainable AI Demo:

**Intelligent Diagnosis and Interpretability of Lung Cancer from CT Images**

[TOC]

## Abstract

Early diagnosis is crucial for reducing lung cancer incidence and mortality. While deep learning has shown promise in classifying lung nodules, neural network decisions often lack interpretability. This project addresses lung cancer detection, classification, and interpretability analysis from chest CT images.

Main Contributions:

1. **Detection and Classification**: Using the Lung-PET-CT-Dx dataset, we trained a Retinanet detection model to identify lung lesions. Subsequently, lesions were classified using ResNet50. We then utilized the LIME algorithm to highlight the critical regions influencing the model’s decisions.
2. **Integrated Interpretability Module**: Innovatively, we integrated a classifier downstream of the detection network, enabling local lesion-level interpretability. This provides not only preliminary pathological classifications but also insights into model decision-making, enhancing clinical trust and efficiency.
3. **Performance**: The detection accuracy for tumor lesions reached 100%, demonstrating excellent localization. Classification accuracy for Adenocarcinoma (AP=0.507) and Squamous Cell Carcinoma (AP=0.523) reached 100% upon excluding atypical cases such as atelectasis. However, Small Cell Lung Cancer showed lower accuracy (AP=0.241), attributed to its imaging characteristics.
4. **Interpretability**: For typical cases, interpretability analysis accurately highlighted lesion features corresponding to Adenocarcinoma and Squamous Cell Carcinoma classifications. Small Cell Lung Cancer interpretability remained limited, consistent with its clinical imaging complexity.

---

Example: **Workflow for Detection and Interpretability Analysis of a Single CT Image Sample**

![image-20250707165614329](C:\Users\chenk\Desktop\Queen's Life\PROJECT\Previous_Work(Explainable_AI)\img\image-20250707165614329.png)

## Methods

### 1 LIME

![image-20250707165746738](C:\Users\chenk\Desktop\Queen's Life\PROJECT\Previous_Work(Explainable_AI)\img\image-20250707165746738.png)

![image-20250707165803356](C:\Users\chenk\Desktop\Queen's Life\PROJECT\Previous_Work(Explainable_AI)\img\image-20250707165803356.png)

### 2 Interpretability Analysis of CT Images using LIME

**The workflow**:

![image-20250707170145989](C:\Users\chenk\Desktop\Queen's Life\PROJECT\Previous_Work(Explainable_AI)\img\image-20250707170145989.png)

Generate Local Perturbation Samples and Construct a New Dataset:

![image-20250707170102509](C:\Users\chenk\Desktop\Queen's Life\PROJECT\Previous_Work(Explainable_AI)\img\image-20250707170102509.png)

## Case Explanation

### 1 Interpretability Analysis of Lung Adenocarcinoma Samples

![image-20250707171916676](C:\Users\chenk\Desktop\Queen's Life\PROJECT\Previous_Work(Explainable_AI)\img\image-20250707171916676.png)

### 2 Interpretability Analysis of Lung Squamous Cell Carcinoma Samples

![image-20250707172027792](C:\Users\chenk\Desktop\Queen's Life\PROJECT\Previous_Work(Explainable_AI)\img\image-20250707172027792.png)

### 3 Feature Regions Noticed by the Model When Explaining Different Classes

![image-20250707172108922](C:\Users\chenk\Desktop\Queen's Life\PROJECT\Previous_Work(Explainable_AI)\img\image-20250707172108922.png)
