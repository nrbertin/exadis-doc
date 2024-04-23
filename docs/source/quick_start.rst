Quick start
===========

**ExaDiS** is implemented using the `Kokkos <https://kokkos.org>`_ framework 
and built using the CMake build system.

Step 1: Install Kokkos
----------------------

To use ExaDiS, first install Kokkos: https://kokkos.org


Step 2: Build ExaDiS
--------------------

* Clone the repository

.. code-block:: console

    git clone https://github.com/LLNL/exadis.git
    cd exadis

* Initialize the submodules (required if enabling the python binding)

.. code-block:: console

    git submodule init
    git submodule update

* Build the code

Examples of building scripts are provided at the root of the exadis project,
e.g. see file ``build_mac.sh``. The Kokkos root path must be specified with option ``-DKokkos_ROOT``.
A typical build instruction will look like:

.. code-block:: console

    mkdir build && cd build
    cmake \
        -DKokkos_ROOT=/path/to/your/kokkos/install/lib/cmake/Kokkos \
        -DCMAKE_CXX_COMPILER=c++ \
        -DPYTHON_BINDING=On \
        ..
    make -j8

.. note::

    Building with nvcc (Cuda) may be pretty slow, please be patient!
    
.. note::

    For additional building options and troubleshooting see section :doc:`installation`.


Step 3: Test your installation
------------------------------

Run an example (assuming ``-DPYTHON_BINDING=On``)

.. code-block:: console

    cd examples/02_frank_read_src
    python test_frank_read_src.py
