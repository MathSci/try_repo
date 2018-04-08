## CHANGE LOG 

*Each file in this project generally has a detailed change log contained 
within itself. This file simply gives a grand overview of such details 
and the annotations in the commits and tags.*


### 2018-04-08  (tag: 1.18.0408)

Add .travis.yml, pure from pandas_datareader repo
which will obviously fail as-is, so edit it.

Add setup.py, currently empty state, else Travis will fail.

Add test_4pytest.py, simplest dummy test,
else no report from pytest generates error in Travis.

pytest command in .travis.yml to include --doctest-module.

.travis.yml: skip DOCBUILD, doctr, and sphinx

matrix section re-written to eventually sunset python27.

Conform to flake8: non-4 indentation and white space 
in arg considered errors.
Remove blank last line per flake8.

In .travis.yml: Use conda instead to install flake8.
Note that flake8 is python-version dependent,
so perhaps better than pip installation.
See http://flake8.pycqa.org/en/latest

Add raw log files from Travis in new log directory.
Instructional to see how jobs are executed in builds.

Useful info on how miniconda installs packages,
which can help to create smaller Docker images
by refactoring code in .travis.yml to Docker files.

The raw log file can be very large due to progress bars
being included. Edit out B/s.*$, then Ctext,
and delete all crtl-[[ characters.

Note: [skip ci] in commit messages will skip Travis.

