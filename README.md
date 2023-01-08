# 123
mot hai ba
ba hai mot
(S)tripe (A)rtifacts (RE)moval in (PY)thon
## Numerical techniques for ring artifact removal in X-ray micro-tomography

**Sarepy** is Python implementation of methods for removing ring artifacts in 
tomography. These methods were published in Optics Express journal; 
Nghia T. Vo, Robert C. Atwood, and Michael Drakopoulos, 
*"Superior techniques for eliminating ring artifacts in X-ray micro-tomography,"* 
Opt. Express 26, 28396-28412 (2018). https://doi.org/10.1364/OE.26.028396.
**Sarepy** is the Python implementations of methods for removing ring artifacts in 
tomography. These implementations were published for the paper; *"Superior techniques 
for eliminating ring artifacts in X-ray micro-to
tarting 05/2021, methods in **Sarepy** have been integrated and developed further in
the **Algotom** package, https://github.com/algotom/algotom . Algotom is a
complete package for processing tomographic data. It is
installable using Conda and Pip.
complete package for processing tomographic data. It is installable using Conda and Pip.

Many utility methods were added to Algotom which allow users to customize 
stripe/ring removal methods as demonstrated [here](https://sarepy.readthedocs.io/toc/section5.html).


How to use
==========
Clone or download the codes to your local machine, then insert the following two lines to your python codes:  

Clone or download the codes to your local machine, then insert the following 
two lines to your python codes: 
```python
import sys  
sys.path.insert(0, "path-to-sarepy-pck")
```

Making sure that the python libs in the requirements.txt are installed before use.  
Details of how to use the methods can be found in /examples/examples.py. Noting that parameters chosen in these examples are for the sinograms in the /data folder. The selected windows of the median filter (81 for large stripes, 31 for others) may be overkill for good quality detectors. You should change these paramaters to suit your data.
Details of how to use the methods can be found in /examples/examples.py. Noting that 
parameters chosen in these examples are for sinograms in the /data folder. 
The selected windows of the median filter (81 for large stripes, 31 for others) 
may be overkill for good quality detectors. You should change these parameters 
to suit your data.

Output of methods is 32-bit data. A viewer software which can display 32-bit tiff image is needed, e.g. [ImageJ](https://imagej.nih.gov/ij/download.html) 
Output of methods is 32-bit data. A viewer software which can display 32-bit tiff 
image is needed, e.g. [ImageJ](https://imagej.nih.gov/ij/download.html) 
or [Fiji](https://imagej.net/software/fiji/downloads).

Features
========

- Methods for cleaning different types of stripe artifacts: full stripes, partial stripes, unresponsive stripes, fluctuating stripes, large stripes, and blurry stripes.
- Various approaches based on the equalization-based methods, i.e equalizing the "response curves" of adjacent pixels, and their combinations.
- A robust stripe detection method.
- Implementations of former methods: a regularization-based method, a normalization-based method, a fft-based method, and a wavelet-fft-based method. 
- Matlab translation of algorithms 3,4,5,6.
- Matlab implementations of algorithms 3,4,5,6.
- Implementations of a basic pipeline of tomography reconstruction: data loading, automated determination of center of rotation, ring artifact removal, tomographic reconstruction, and data saving.
- Postprocessing methods for removing ring artifacts: polar tranformation, fft-based methods.
- Postprocessing methods for removing ring artifacts: polar transformation, fft-based methods.

Documentation
=============
- https://sarepy.readthedocs.io/

- https://sarepy.readthedocs.io/
