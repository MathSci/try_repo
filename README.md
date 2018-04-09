## try_repo : ALPHA status forever

[![Build Status](https://travis-ci.org/MathSci/try_repo.svg?branch=master)](https://travis-ci.org/MathSci/try_repo)

- **Dummy repo to test Travis CI and GitHub continuous integration.**
- Create test environment for Python and Miniconda.
    - Prepare code for migration from python27 to python3.
- Test Travis for pip versus conda installations.
- Use `pytest` for unit testing.
- Use `flake8` for Python linting.
- *Find essential and minimal requirements for successful* ***build***.


### Programming Travis

The Travis continuous integration process
is summed up in a dot file called `.travis.yml`
to be placed at the top directory within a git repository.
There are some useful tricks in writing such a 
[YAML](https://en.wikipedia.org/wiki/YAML) file,
especially where a complex scientific stack is needed.
For the Python ecosystem, the Anaconda distribution
saves us from the hell of dependencies which involves
binaries necessary for computational speed.
We shall install miniconda prior to
installing only what is essential to a particular project.
See our https://git.io/travis for a reasonable example.

Travis is agnostic about the testing utilities.
We could have alternatively used `nose` and `pylint`,
instead of `pytest` and `flake8`.

Travis is run on containers and virtual machines
based on Ubuntu (14.04 has code name *trusty*),
so the scripting within the YAML file are shell commands.


### Build status

Watch the status of interim builds at https://travis-ci.org/MathSci/try_repo/builds

***Why ALPHA status forever?***
There will be many *fails* to determine whether the tests and jobs 
are actually detecting *intentional* errors.
Find the last successful build to retrieve a reliable `.travis.yml` 
file to serve as your starting point.

Tip: What you learn from a successful Travis build can also be used
to write an effective Docker container file.

The summary logs will show how specific utilities,
such as pytest and flake8, report back to Travis.
The raw logs are interesting if you need to see 
the fine details of the various installations.


### References

-  YAML Ain't Markup Language: https://en.wikipedia.org/wiki/YAML
-  For Travis newbies: https://docs.travis-ci.com/user/for-beginners
-  Python setup: https://docs.travis-ci.com/user/languages/python
-  Install dependencies: https://docs.travis-ci.com/user/installing-dependencies
-  Travis customization: https://docs.travis-ci.com/user/customizing-the-build
-  Notifications from Travis: https://docs.travis-ci.com/user/notifications

---

Last update : 2018-04-09

