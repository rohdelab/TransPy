# PyTransKit
Python Transport Based Signal Processing Toolkit

Website and documentation: https://pytranskit.readthedocs.io/


## Installation
The library could be installed through pip
```
pip install pytranskit
```
Alternately, you could clone/download the repository and add the `pytranskit` directory to your Python path
```
import sys
sys.path.append('path/to/pytranskit')

from pytranskit.optrans.continuous.cdt import CDT
```

## Transport-based Transforms
### Cumulative Distribution Transform (CDT)
#### Definition
Let <img src="https://latex.codecogs.com/svg.latex?s(x),x\in\Omega_{s}\subset\mathbb{R}" title="s(x),x\in\Omega_{s}\subset\mathbb{R}" align=center> be a positive density function (PDF). The CDT of the PDF <img src="https://latex.codecogs.com/svg.latex?s(x)" title="s(x)" align=center> with respect to a reference PDF <img src="https://latex.codecogs.com/svg.latex?s_0(x),x\in\Omega_{s_0}\subset\mathbb{R}" title="s_0(x),x\in\Omega_{s_0}\subset\mathbb{R}" align=center> is given by the mass preserving function <img src="https://latex.codecogs.com/svg.latex?\widehat{s}(x)" title="\widehat{s}(x)" align=center> that satisfies - 

<img src="https://latex.codecogs.com/svg.latex?\int_{\inf(\Omega_s)}^{\widehat{s}(x)}&space;s(u)du&space;=&space;\int_{\inf(\Omega_{s_0})}^{x}&space;s_0(u)du" title="\int_{\inf(\Omega_s)}^{\widehat{s}(x)} s(u)du = \int_{\inf(\Omega_{s_0})}^{x} s_0(u)du" align=center>

which yields 

<img src="https://latex.codecogs.com/svg.latex?\widehat{s}(t)&space;=&space;S^{-1}(S_0(t))" title="\widehat{s}(t) = S^{-1}(S_0(t))" align=center>,

where, <img src="https://latex.codecogs.com/svg.latex?S(t)=\int_{-\infty}^{x}s(u)du" title="S(t)=\int_{-\infty}^{x}s(u)du" align=center>    and    

<img src="https://latex.codecogs.com/svg.latex?S_0(t)=\int_{-\infty}^{x}s_0(u)du" title="S_0(t)=\int_{-\infty}^{x}s_0(u)du" align=center>

The inverse transform of the CDT <img src="https://latex.codecogs.com/svg.latex?\widehat{s}(x)" title="\widehat{s}(x)" align=center> is given by,

<img src="https://latex.codecogs.com/svg.latex?s(x)=(\widehat{s}^{-1}(x))'s_0(\widehat{s}^{-1}(x))" title="s(x)=(\widehat{s}^{-1}(x))'s_0(\widehat{s}^{-1}(x))" align=center>

#### Tutorial
- Cumulative Distribution Transform (CDT) tutorial [[notebook](https://github.com/rohdelab/PyTransKit/blob/master/tutorials/01_tutorial_cdt.ipynb)] [[nbviwer](https://nbviewer.jupyter.org/github/rohdelab/PyTransKit/blob/master/tutorials/01_tutorial_cdt.ipynb)]

### Radon-Cumulative Distribution Transform (R-CDT)
#### Definition

#### Tutorial
- Radon-CDT tutorial [[notebook](https://github.com/rohdelab/PyTransKit/blob/master/tutorials/02_tutorial_rcdt.ipynb)] [[nbviewer](https://nbviewer.jupyter.org/github/rohdelab/PyTransKit/blob/master/tutorials/02_tutorial_rcdt.ipynb)]
- 3D Radon-CDT tutorial [[notebook](https://github.com/rohdelab/PyTransKit/blob/master/tutorials/05_tutorial_rcdt3D.ipynb)][[nbviewer](https://nbviewer.jupyter.org/github/rohdelab/PyTransKit/blob/master/tutorials/05_tutorial_rcdt3D.ipynb)]

### Continuous Linear Optimal Transport Transform
#### Definition

#### Tutorial
- Continuous Linear Optimal Transport Transform (CLOT) tutorial [[notebook](https://github.com/rohdelab/PyTransKit/blob/master/tutorials/07_tutorial_clot.ipynb)] [[nbviewer](https://nbviewer.jupyter.org/github/rohdelab/PyTransKit/blob/master/tutorials/07_tutorial_clot.ipynb)]

## Applications
### Classification Examples
- CDT Nearest Subspace (CDT-NS) classifier for 1D data [[notebook](https://github.com/rohdelab/PyTransKit/blob/master/tutorials/04_tutorial_CDT-NS_classifier.ipynb)] [[nbviewer](https://nbviewer.jupyter.org/github/rohdelab/PyTransKit/blob/master/tutorials/04_tutorial_CDT-NS_classifier.ipynb)]
- Radon-CDT Nearest Subspace (RCDT-NS) classifier for 2D data [[notebook](https://github.com/rohdelab/PyTransKit/blob/master/tutorials/03_tutorial_RCDT-NS_classifier.ipynb)] [[nbviewer](https://nbviewer.jupyter.org/github/rohdelab/PyTransKit/blob/master/tutorials/03_tutorial_RCDT-NS_classifier.ipynb)]
- 3D Radon-CDT Nearest Subspace (3D-RCDT-NS) classifier for 3D data [[notebook](https://github.com/rohdelab/PyTransKit/blob/master/tutorials/06_tutorial_3DRCDT-NS_classifier.ipynb)] [[nbviewer](https://nbviewer.jupyter.org/github/rohdelab/PyTransKit/blob/master/tutorials/06_tutorial_3DRCDT-NS_classifier.ipynb)]

### Estimation Examples
- Time delay estimation using CDT [[notebook](https://github.com/rohdelab/PyTransKit/blob/master/Examples/Example01_estimation_delay.ipynb)] [[nbviewer](https://nbviewer.jupyter.org/github/rohdelab/PyTransKit/blob/master/Examples/Example01_estimation_delay.ipynb)]
- Time delay and linear dispersion estimation using CDT [[notebook](https://github.com/rohdelab/PyTransKit/blob/master/Examples/Example02_estimation_delay_linear_dispersion.ipynb)] [[nbviewer](https://nbviewer.jupyter.org/github/rohdelab/PyTransKit/blob/master/Examples/Example02_estimation_delay_linear_dispersion.ipynb)]

## Resources
- External website http://imagedatascience.com/transport/

