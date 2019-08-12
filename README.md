# pnlpipe_software submodule


This module is used as a submodule to install required software for [**pnlpipe**](https://github.com/pnlbwh/pnlpipe) and [**pnlNipype**](https://github.com/pnlbwh/pnlNipype) installation.

    
Defining `PYTHONPATH` like below enables `from pnlpipe_software import *` inside the software 
installation scripts.

    export PYTHONPATH=/abs/directory/of/pnlpipe_software/
    

The python scripts in this module download and install software. 
They are essentially wrapper around `git`, `cmake`, and `make` commands.


If you would like to use this submodule separately from **pnlpipe** or **pnlNipype**, 
you should clone the submodule `https://github.com/pnlbwh/cmd.git` and use `cmd/install.py` script.
    
    git clone https://github.com/pnlbwh/cmd.git
    git clone https://github.com/pnlbwh/pnlpipe_software.git
    
Then upon defining `PYTHONPATH` and `PNLPIPE_SOFT`, you can install software as follows:

    export PYTHONPATH=/abs/directory/of/pnlpipe_software/
    export PNLPIPE_SOFT=/directory/for/software/    # this is where software modules are installed
    
    cmd/install.py -h                               # see usage
    cmd/install.py UKFTractography                  # install default branch
    cmd/install.py -v master dcm2niix               # install master branch
    cmd/install.py ANTs -v 6f403d7                  # install release/branch defined by hash
    
    

**NOTE** Support for the following scripts are deprecated because they are not used with *pnlpipe/pnlNipye* anymore:
  
* FreeSurfer.py
* HCPPipelines.py
* Slicer.py
* mrtrix3.py
* nrrdchecker.py
* whitematteranalysis.py


 