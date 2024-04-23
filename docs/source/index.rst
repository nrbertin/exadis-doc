Welcome to ExaDiS documentation!
===================================

**ExaDiS** (Exascale Dislocation Simulator) is a set of software modules written
to enable numerical simulations of large groups of moving and interacting dislocations,
line defects in crystals responsible for crystal plasticity. By tracking time evolution
of sufficiently large dislocation ensembles, ExaDiS predicts plasticity response and
plastic strength of crystalline materials.

**ExaDiS** is built around a portable library of core functions for Discrete Dislocation 
Dynamics (DDD) method specifically written to perform efficient computations on new HPC
architectures (e.g. GPUs). Simulations can be driven through the C++ or python interfaces.
The python binding module can also be interfaced with the upcoming `OpenDiS 
<https://github.com/opendis/>`_ framework.

.. note::

    Although ExaDiS is a fully functional code, it is currently under active development 
    and is subject to frequent updates and bug fixes. There is no guarantee of stability 
    and one should expect occasional breaking changes to the code.


Contents
--------

.. toctree::
    :maxdepth: 1

    quick_start
    installation
    user_guide
    developer_guide
