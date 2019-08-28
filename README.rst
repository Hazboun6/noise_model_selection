NANOGrav Noise Model Selection Code Bank
----------------------------------------

Code bank and tutorials for NANOGrav noise model selection.

Software Dependencies
---------------------

The notebooks herein are dependent on the pulsar timing array data analysis suite
`enterprise <https://github.com/nanograv/enterprise>`_ and the software package
`enterprise_extensions <https://github.com/stevertaylor/enterprise_extensions>`_
containing a number of scripts and models useful for PTA analysis. This
`Dropbox Paper <https://paper.dropbox.com/doc/So-you-want-to-install-enterprise--AjVKn5a1QX594YH31gj5ymUkAQ-uhmTCxW0wm7mkCaanMwtx>`_
contains information for installing this software.

In addition to the post processing functions available in enterprise_extensions
the plotting functions available in
`la_forge <https://github.com/Hazboun6/la_forge>`_ will be used in these notebooks.

Pulsar Timing Array Data Analysis
---------------------------------

For those new to pulsar timing array data analysis there are a number of
repositories of workshop materials and tutorials available.

The NANOGrav
`Pulsar Timing School <https://github.com/nanograv/pulsar_timing_school>`_
repository contains a number of activities and a comprehensive literature review
of various gravitational wave data analysis papers.

The International Pulsar Timing Array
`GW Tutorials <https://github.com/ipta/gwa_tutorials>`_ repository has a number
extensive tutorials for using `enterprise` and `enterprise_extensions`. There is
also a tutorial for using `libstempo <https://github.com/vallis/libstempo>`_, a Python
wrapper for the pulsar timing software ``TEMPO2``.

## Noise Model Notes
There are a number of different kernels we use to model the time-correlated
noise in our pulsars. This
`pdf <https://raw.githubusercontent.com/Hazboun6/nanograv_noise_model_selection/master/Enterprise_Noise_Model_Notes.pdf>`
discusses the ones currently supported by
``enterprise_extensions``.

Users Guide
-----------
In order to facilitate the sharing of changes to this software the following we
make the following suggestions:

After cloning the repo to your local machine, change directories and make a branch
of the repository with ``YOURINITIALS-working``:
::

    git clone https://github.com/Hazboun6/nanograv_noise_model_selection.git
    cd nanograv_noise_model_selection
    git checkout -b jsh-working

This will allow more control when trying to make pull requests for changing the
code. In addition, the ``outdir`` for the `PTMCMCSampler` is set as
``chains/``. Please keep this as the outmost directory for any sampling
chains, as the ``.gitignore`` will ignore all files in that directory.
