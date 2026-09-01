# Parareal-OCP-Convergence-tests-bachelor-thesis

This repository contains every piece of code, that was necessary to produce the results in the Bachelorthesis.

1. OCP_algorithm.ipynb:
   - This is the OCP algorithm, presented in chapter 3 of the thesis. It is modified, such that one can change
   - the degrees of numerator and denominator of the stability function.
  
2. Parareal_algorithm.ipynb:
   - This notebook only contains the parareal algorithm itself, without computing the error to the fine solution at every         - iteration. It also contains a legend of the inputs that the parareal algorithm uses/ a list of all precompued values.
  
3. parareal_grundfunktionen.py:
   - This file contains all auxillary functions that are needed to make the parareal algorithm, and all the tests run.
   - more detailed information on the defined functions are given in file itself or the notebook of the same name.
   - Included are FEM in 1D, propagators, functions that compute the propagator sequentially, error functions for verification,
   - and functions for precalculation for the parareal algorithm
  
4. Tables_in_section_5.ipynb:
   - This notebook contains the calculation of the values, presented in the two tables at the end of section 5.
  
5. propagators.py:
   - This file contains all common FPs and CPs that have been used throughout this work, together with a dictionary entry at
   - the end to easy call them in other notebooks

6. Examples_from_section5.ipynb:
   - This notebook contains 3 example plots, which are all part of the numerical experiments in Section 5.

7. Additional_plots_section_4and5:
   - This notebook contains the rest of the plots that have been shown throughout section 3,4 and 5. Together with
   - Examples_from_section5-ipynb, every plot that has been shown in the thesis can be recreated.

8. modules:
modules contains additional .pt files, which contain the prarameters for the stability functions that were used to create
   - the plots in sections 3,4 and 5. The OCP algorithm saves them at the end to avoid additional round off errors. Also due
   - to this, one should be able to run the experiments without the need of optimizing the coarse propagator again. The files
   -  mostly follow the same naming convention: for example: "n1m2_001_100_LOBATTOIIIC4_J20.pt"
   -  n1m2 is for the degrees of numerator and denominator of the stability function
   -  001_100 is for the set it has beeon optimized on, most of it are
   -  either on of two: "001_100" for [0.01,100] or "exact_eig" for the explicit eigenvalues of the discrete operators
   -  LOBATTOIIIC4 is for the FP it has been trianed for, following the names from propagators.py, the number at the end is
   -  the stage
   -  J is the ration it has been trianed for
   -  some ahve a_100 or a_10000 at the end, this was done for Example 5.3, to make further distinctions, if the were trained
   -  on the exact eigenvlaues
        - modules contains additional .pt files, which contain the prarameters for the stability functions that were used to create
   - the plots in sections 3,4 and 5. The OCP algorithm saves them at the end to avoid additional round off errors. Also due
   - to this, one should be able to run the experiments without the need of optimizing the coarse propagator again. The files
   -  mostly follow the same naming convention: for example: "n1m2_001_100_LOBATTOIIIC4_J20.pt"
   -  n1m2 is for the degrees of numerator and denominator of the stability function
   -  001_100 is for the set it has beeon optimized on, most of it are
   -  either on of two: "001_100" for [0.01,100] or "exact_eig" for the explicit eigenvalues of the discrete operators
   -  LOBATTOIIIC4 is for the FP it has been trianed for, following the names from propagators.py, the number at the end is
   -  the stage
   -  J is the ration it has been trianed for
   -  some ahve a_100 or a_10000 at the end, this was done for Example 5.3, to make further distinctions, if the were trained
   -  on the exact eigenvlaues
     
9. Use of AI/ code from other sources:
The implementation in "OCP_algorithm.ipynb" is largely based on and adapted
from the GitHub repository accompanying the original paper on the OCP algorithm.
The implementation was modified for this thesis, in particular to allow different
degrees of the numerator and denominator of the stability function and to use a
different stopping criterion.

The functions used for the Parareal implementation in
"parareal_grundfunktionen.py" and "Parareal_algorithm.ipynb" were written by
the author. OpenAI ChatGPT was used as an auxiliary tool for debugging and
identifying programming errors.

AI was additionally used to generate some repetitive parts of the code, for
example parts of "propagators.py" and repeated function calls for creating plots,
where only input files, output files, or similar parameters had to be changed.
All AI-assisted code was reviewed and verified by the author.
