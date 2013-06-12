feasiblesets 
============

Research code for understanding distributions of wealth in the context of all possible distributions.

Files and Folders
-----------------

1. FEASIBLE_FUNCTIONS   --Cython version of feasible_functions.py. Converting a .py file to .pyx (Cython) 
requires addtional files (see: http://docs.cython.org/src/userguide/tutorial.html).
Note, the feasible_functions.pyx file as well as feasible_functions.py (depending on whether the user
want to run in Cython or pure Python) require the macroecotools module that is provided in this repository.

2. public_data --folder containing public data and data files (observed vs predicted sads)

3. Locey-White_2013.py  --Python file that recreates all figures in the main body of Locey and White (2013).
Currently calls feasible_functions module from the FEASIBLE_FUNCTIONS directory, but can also be set to 
use the feasible_functions.py file.

4. combine_macrostates.py --Python script that combines random generated macrostates from several folders.
For example, if multiple machines have generated files of macrostates matching N-S combinations, we will
to combine the macrostates into a single file holding all of them.



blip
blip,
check back later


License
-------

feasiblesets is licensed under the open source MIT License

Copyright (c) 2012 Weecology

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Contact information
-------------------
Ken Locey's email: ken@weecology.org and locey@biology.usu.edu

*Go to [Ken's website](kenlocey.wordpress.com)*

Included files
-------------------------

* Python modules (feasible_functions.py) to generate and examine feasible sets and random macrostates thereof
* Python scripts to reproduce results and figures used by Locey and White (in final prep)
* Cython setup files
* A dictionary of random macrostates (if we can overcome size restrictions). This would be expensive for others to reproduce.
* A documentation file to describe what all this feasible set stuff is for



Programs and packages used by the authors
-------------------------------

Python version 2.6.5 or higher
Cython
Sage version 4.7.2 or higher


Cython
------

Cython is a language that makes writing C extensions for the Python language as easy as Python itself.
It is based on the well-known Pyrex, but supports more cutting edge functionality and optimizations.
*http://www.cython.org/*  
setup tutorial: *http://docs.cython.org/src/userguide/tutorial.html*

Most any Python script can be run at C speeds by:
* replacing the .py extension in your script with .pyx
* create a setup file. To save the user a hassle, we have made several setup files for scripts in this repository.
* run this command from within the folder containing the .pyx file and the setup file:


        python setup_thescriptsname.py build_ext --inplace

iPython and iPython Notebook
----------------------------

We are currently rescripting copies of repository files to be used in iPython Notebook. Running scripts in
iPython notebook will enable users to read comments in a convenient form, run blocks of code, and visualize
results between blocks of code. 

The biggest problem is that most of the scripts in this repository use Sage, and calling Sage within the iPython
notebook is going to take some thinking.
