# MLforSTCP
Machine Learning workflow for accelerating the design of Synthesizable Thermally Conductive Polymers.
## Description
Machine learning framework for the generation of highly thermally conductive polymers using a rule-based polymer generator, involving four components: benchmark dataset, quantitative structure-property relationships (QSPR) models, polymer generator, and virtual screening.![Framework](https://github.com/huangxiang701/MLforSTCP/blob/main/workflow.jpg)

## Requirements

````
git clone https://github.com/SJTU-MI/PMBO.git
````

To run most code in this repository, the relevant anaconda environment can be installed from environment.yml. To build this environment, run：<br>
````
cd ./PMBO
conda env create -f environment.yml
conda activate pmbo
````
Additionally, polymer physical feature engineering and properties calculations can be accessed at other GitHub repositories of [APFEforPI](https://github.com/SJTU-MI/APFEforPI) and [RadonPy](https://github.com/RadonPy/RadonPy).
## Try the desired parts of the project:
### Code in the pmbo folder
**gp.py**: Gaussian process regression model <br>
**Acq_fun.py**: Acquisition functions such as EI(expected improvement) and UCB(upper confidence bound) <br>
**hypervolume.py**: Calculation of hypervolume <br>
**utility.py**: Utility functions such as Pareto front allocation and data pre/post processing <br>
**optimize.py**: Core of multi-objective Bayesian optimization <br>
**log.py**: PMBO Logo <br>
### Tutorial
**MBO_tutorial.ipynb**: A case of multi-objective optimization for multifunctional polymers discovery <br>
**example.csv**:Benchmark dataset for testing (input file) <br>
**cal_data.csv**: MBO recommended polymers and their observed properties (output file) <br>
**HV.csv**: Optimized convergence curve evaluated by hypervolume (output file) <br>
## Authors

| **AUTHORS** |Xiang Huang, Shenghong Ju            |
|:-------------:|--------------------------------------------------|
| **VERSION** | V1.0 / July,2023                               |
| **EMAILS**  | shenghong.ju@sjtu.edu.cn                         |
| **GROUP HOME**  | https://ju.sjtu.edu.cn/en/                         |

## Attribution
This work is under BSD-2-Clause License. Please, acknowledge use of this work with the appropiate citation to the repository and research article.
