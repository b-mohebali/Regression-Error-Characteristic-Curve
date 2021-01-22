[![build status](https://travis-ci.com/slickml/slick-ml.svg?branch=master)](https://travis-ci.com/github/slickml/slick-ml)
[![License](https://img.shields.io/github/license/slickml/slick-ml)](https://github.com/slickml/slick-ml/blob/master/LICENSE/)
[![PyPI - Downloads](https://img.shields.io/pypi/dm/slickml)](https://pypi.org/project/slickml/)
![PyPI Version](https://img.shields.io/pypi/v/slickml)
[![Forks](https://img.shields.io/github/forks/slickml/slick-ml)](https://github.com/slickml/slick-ml/network/members/)
[![Stars](https://img.shields.io/github/stars/slickml/slick-ml)](https://github.com/slickml/slick-ml/stargazers/)


<h1 align="center">
    Regression Error Characteristic Curve in Python
</h1>


**Regression Error Characteristic (REC)** curves can be used to visualize 
the performance of the regressor models. REC
illustrates the absolute deviation tolerance versus the fraction
of the exemplars predicted correctly within the tolerance interval. 
The resulting curve estimates the cumulative distribution
function of the error. The area over the REC curve (AOC),
which can be calculated via the area under the REC curve
(AOC = 1 - AUC) is a biased estimate of the expected
error. Furthermore, the coefficient of determination R2 can
be also calculated with respect to the AOC [Reference 1]. Likewise the
ROC curve, the shape of the REC curve can also be used
as a guidance for the users to reveal additional information
about the data modeling. The REC curve was implemented
in Python and the details of the error metrics and scaling of
the residuals are also available [Reference 2].


## Quick Start
Here is an exmple of using REC:
```python
# run feature selection using loaded data
from src.rec import RegressionErrorCharacteristic
myREC = RegressionErrorCharacteristic(y_true, y_pred)
myREC.plot_rec()
```
![rec](https://raw.githubusercontent.com/amirhessam88/Regression-Error-Characteristic-Curve/master/assets/plot.png)

This algorithm is also implemented in more details in **SlickML** library. 

## Installation

First, install Python 3.6 from https://www.python.org, and then run:

```
pip install slickml
```

Here is an example using SlickML to quickly visualize the regression metrics:

```python
# plot regression metrics
from slickml.metrics import RegressionMetrics
reg_metrics = RegressionMetrics(y_test, y_pred)
reg_metrics.plot()
```
![regmetrics](https://raw.githubusercontent.com/amirhessam88/Regression-Error-Characteristic-Curve/master/assets/slickml.png)

## Citing **REC**
If you use REC in academic work, please consider citing
https://doi.org/10.1117/12.2304418 .

### Bibtex Entry:
```bib
@inproceedings{tahmassebi2018ideeple,
  title={ideeple: Deep learning in a flash},
  author={Tahmassebi, Amirhessam},
  booktitle={Disruptive Technologies in Information Sciences},
  volume={10652},
  pages={106520S},
  year={2018},
  organization={International Society for Optics and Photonics}
}
```
### APA Entry:

Tahmassebi, A. (2018, May). ideeple: Deep learning in a flash. In Disruptive
Technologies in Information Sciences (Vol. 10652, p. 106520S). International
Society for Optics and Photonics.

