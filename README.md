# pulsar_docker
Builds a docker image for a pulsar analysis packages and few extras on Ubuntu 16.04 LTS.

# Includes
- calceph
- ds9
- fv
- psrcat
- tempo
- tempo2
- psrchive
- sofa c-library
- sofa fortran-library
- sigproc
- sigpyproc
- h5check
- dal
- dspsr
- GeographicLib
- h5edit
- fitsverify
- psrsalsa
- pypsrfits
- presto
- wapp2psrfits
- psrfits2psrfits
- psrfits_utils
- pyslalib
- vpsr
- gpy
- coast_guard
- setuptools
- numpy
- scipy
- pandas
- h5py
- fitsio
- astropy
- astroplan
- pytz
- paramz
- aplpy
- pyfits
- peakutils
- pymc
- matplotlib
- seaborn
- lmfit
- pyephem
- and all their dependencies (pgplot5, fftw, etc)

You'll find all pulsar software in /home/psr/software, environment variables are set according to ~/.mysetenv.bash file.

# Using
To build:

    docker build -t stock_complete_suite .

To run image:

    docker run -it stock_complete_suite /bin/bash

To mount data directory into the docker container with the -v flag:

    docker run -it -v <data_location>:/data stock_complete_suite /bin/bash

This will drop you in to an ubuntu os with bash shell with all data in /data.

To run the image with X11 and mounted data directory, run the container first:

    docker run -p 2222:22 -v <data_location>:/data stock_complete_suite

Check if container is running with docker ps -a. You can log in using **psr** as password:

    ssh -XY psr@localhost -p 2222

# Issues
Report problems to mserylak@gmail.com.
