#Scikit-learn

scikit-learn is a Python module for machine learning built on top of SciPy and distributed under the 3-Clause BSD license.

The project was started in 2007 by David Cournapeau as a Google Summer of Code project, and since then many volunteers have contributed. See the AUTHORS.rst file for a complete list of contributors.

It is currently maintained by a team of volunteers.

Note scikit-learn was previously referred to as scikits.learn.

Important links
Official source code repo: https://github.com/scikit-learn/scikit-learn
HTML documentation (stable release): http://scikit-learn.org
HTML documentation (development version): http://scikit-learn.org/dev/
Download releases: http://sourceforge.net/projects/scikit-learn/files/
Issue tracker: https://github.com/scikit-learn/scikit-learn/issues
Mailing list: https://lists.sourceforge.net/lists/listinfo/scikit-learn-general
IRC channel: #scikit-learn at irc.freenode.net
Dependencies
scikit-learn is tested to work under Python 2.6, Python 2.7, and Python 3.4. (using the same codebase thanks to an embedded copy of six). It should also work with Python 3.3.

The required dependencies to build the software are NumPy >= 1.6.1, SciPy >= 0.9 and a working C/C++ compiler. For the development version, you will also require Cython >=0.23.

For running the examples Matplotlib >= 1.1.1 is required and for running the tests you need nose >= 1.1.2.

This configuration matches the Ubuntu Precise 12.04 LTS release from April 2012.

scikit-learn also uses CBLAS, the C interface to the Basic Linear Algebra Subprograms library. scikit-learn comes with a reference implementation, but the system CBLAS will be detected by the build system and used if present. CBLAS exists in many implementations; see Linear algebra libraries for known issues.

Install
This package uses distutils, which is the default way of installing python modules. To install in your home directory, use:

python setup.py install --user
To install for all users on Unix/Linux:

python setup.py build
sudo python setup.py install
For more detailed installation instructions, see the web page http://scikit-learn.org/stable/install.html

Development
Code
GIT
You can check the latest sources with the command:

git clone https://github.com/scikit-learn/scikit-learn.git
or if you have write privileges:

git clone git@github.com:scikit-learn/scikit-learn.git
Contributing
Quick tutorial on how to go about setting up your environment to contribute to scikit-learn: https://github.com/scikit-learn/scikit-learn/blob/master/CONTRIBUTING.md

Before opening a Pull Request, have a look at the full Contributing page to make sure your code complies with our guidelines: http://scikit-learn.org/stable/developers/index.html

Testing
After installation, you can launch the test suite from outside the source directory (you will need to have the nose package installed):

$ nosetests -v sklearn
Under Windows, it is recommended to use the following command (adjust the path to the python.exe program) as using the nosetests.exe program can badly interact with tests that use multiprocessing:

C:\Python34\python.exe -c "import nose; nose.main()" -v sklearn
See the web page http://scikit-learn.org/stable/install.html#testing for more information.

Random number generation can be controlled during testing by setting the SKLEARN_SEED environment variable.
