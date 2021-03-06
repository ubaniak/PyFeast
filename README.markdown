# PyFeast
Python bindings to the FEAST Feature Selection Toolbox.

## About PyFeast
PyFeast is a interface for the FEAST feature selection toolbox, which was
originally written in C with a interface to Matlab.

Because Python is also commonly used in computational science, writing bindings 
to enable researchers to utilize these feature selection algorithms in Python 
was only natural.

At Drexel University's [EESI Lab](http://www.ece.drexel.edu/gailr/EESI/), we are using PyFeast to create a feature
selection tool for the Department of Energy's upcoming KBase platform.

## Requirements
In order to use the feast module, you will need the following dependencies

* Python 2.7
* Numpy
* Linux or OS X 

## Installation
To install the FEAST interface, you'll need to build and install the FEAST
libraries first, and then install python.

Make MIToolbox and install it:

    cd FEAST/MIToolbox
    make
    sudo make install

Make FSToolbox and install it:

    cd FEAST/FSToolbox
    make
    sudo make install

Run ldconfig to update your library cache:
    
    sudo ldconfig

Install our PyFeast module:

    python ./setup.py build
    sudo python ./setup.py install

## Demonstration
See test/test.py for an example with uniform data and an image
data set. The image data set was collected from the digits example in 
the Scikits-Learn toolbox.

## References
* [FEAST](http://www.cs.man.ac.uk/~gbrown/fstoolbox/) - The Feature Selection Toolbox  
* [Fizzy](http://www.kbase.us/developer-zone/api-documentation/fizzy-feature-selection-service/)  - A KBase Service for Feature Selection
* [Conditional Likelihood Maximisation: A Unifying Framework for Information Theoretic Feature Selection]
(http://jmlr.csail.mit.edu/papers/v13/brown12a.html) 
