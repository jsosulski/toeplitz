# toeplitz
### Python wrapper for Fortran90 toeplitz package to solve a variety of Toeplitz and circulant linear systems

The wrapped Fortran90 toeplitz package was written by John Burkardt and is distributed under GNU LGPL license.
It can be obtained from [John Burkhardt's website][1].
There you can additionally find a short documentation and the following description:
> TOEPLITZ is a FORTRAN90 library which solves a variety of Toeplitz and circulant linear systems.
The package can also handle circulant Toeplitz systems, and some other more complicated but related forms.
The TOEPLITZ package was written in the early 1980's by a joint working group of American and Soviet mathematicians.
The original, true, correct version of TOEPLITZ is available in the TOEPLITZ subdirectory of the NETLIB web site.

This wrapper is based on numpy/f2py and provides a python interface for all fortran subroutines *_sl.
Only the functions sto_sl and cto_sl (solve linear Toeplitz systems) are tested.
They provide acceptable accuracy compared to scipy.linalg and run faster for large inputs.
All other routines are not tested, but should work.
For more documentation than on John Burkardt's website check the source file toeplitz.f90.

### Installation

After installing the required [NumPy][2] package you can install via [pip][3]
by running

    pip install toeplitz

Alternatively download the source code and run
   
    python setup.py install

The tests can be run with the script (SciPy installation necessary)  
   
    toeplitz-runtests

[1]: http://people.sc.fsu.edu/~jburkardt/f_src/toeplitz/toeplitz.html
[2]: http://www.numpy.org/
[3]: http://www.pip-installer.org/