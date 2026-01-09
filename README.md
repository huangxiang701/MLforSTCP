# MLforSTCP
Machine Learning workflow for accelerating the design of Synthesizable Thermally Conductive Polymers.

## Description
Machine learning framework for the generation of highly thermally conductive polymers using a rule-based polymer generator, involving four components: benchmark dataset, quantitative structure-property relationships (QSPR) models, polymer generator, and virtual screening.![Framework](https://github.com/huangxiang701/MLforSTCP/blob/main/workflow.jpg)

## Requirements
### 1. Installation of requirement packages 
  - python==3.7.1
  - tensorflow==2.3.0
  - scikit-learn==1.0.2
  - rdkit==2020.09.1
  - pandas==1.2.4
  - numpy==1.21.5

### 2. Installation of other dependency packages
Since a higher Python version is required, please create a new environment.
#### SMiPoly [[link](https://github.com/PEJpOhno/SMiPoly)] [[paper](https://pubs.acs.org/doi/10.1021/acs.jcim.3c00329)]
````
pip install smipoly==0.1.0
````
#### RadonPy [[link](https://github.com/RadonPy/RadonPy)] [[paper](https://www.nature.com/articles/s41524-022-00906-4)]
````
pip install radonpy-pypi==0.2.9
````

## Try the desired parts of the project:
### Codes
**01Cal_FF_descriptor.ipynb**: Calculation of kernel mean force field descriptors via RadonPy. <br>
**02Rea_polymer.ipynb**: Virtual synthesis of polymers based on reaction rules using SMiPoly (polyolefins as an example). <br>
**03CNN.ipynb**: Convolutional neural network for mapping descriptors to thermal conductivity. <br>
**04FFNN.ipynb**: Feedforward neural network for mapping descriptors to thermal conductivity. <br>
**05Prediction.ipynb**: Applying the trained DNN models to predict the thermal conductivity of newly synthesized polymers (polyester as an example). <br>

### Datasets
**Benchmark**: The benchmark dataset serves for DNN models training. <br>
**Reaction**: Virtual polymer collections generated based on reaction rules. <br>
**ML_model**: Trained CNN and FFNN models. <br>
**Prediction**: DNN prediction of thermal conductivity for six types of virtual synthetic polymers. <br>
**Verification**: Molecular dynamics verification of thermal conductivity results for selected polymers. <br>

## Related projects
**1. SMiPoly** (Generation of a Synthesizable Polymer Virtual Library Using Rule-Based Polymerization Reactions)
https://github.com/PEJpOhno/SMiPoly<br>
**2. RadonPy** (Fully Automated Calculation for a Comprehensive Set of Polymer Properties)  
https://github.com/RadonPy/RadonPy<br>
**3. SPACIER** (On-Demand Polymer Design with MD and ML)  
https://github.com/s-nanjo/Spacier/

## Attribution
This work is under BSD-2-Clause License. Please, acknowledge use of this work with the appropiate citation to the repository and research article.
