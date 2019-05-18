# Python Pyramid Setup and Tutorials:
![stem](https://s3-ap-southeast-2.amazonaws.com/stem-formatics/stem_formatics.PNG)
### Setup:

Running on AWS CLoud 9

OS: Ubuntu 18.04.2 LTS
Packages for setup: pip 9.0.1,Python 2.7.15rc1,python-venv

-set an environment variable to where you want your virtual environment.

$ export VENV=~/env

-create the virtual environment.

$ python3 -m venv $VENV

-install pyramid.

$ $VENV/bin/pip install pyramid

-or for a specific released version.

$ $VENV/bin/pip install "pyramid==1.10.4"