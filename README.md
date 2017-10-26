# betanb6

NBODY6++GPU (Spurzem et al. 1999, Aarseth 2003, Wang et al. 2015) with HDF5 output facilities.

To enable HDF5 output, config the code with the ``--enable-hdf5`` flag.
```
./configure --enable-hdf5
make
```
Make sure that your HDF5 library is configured with the ``--enable-fortran --enable-parallel`` flags.

Use ``KZ(46)`` and ``KZ(47)`` to adjust the HDF5 output frequency. Normally, it is recommended to set ``KZ(46)=3``. ``KZ(47)`` determines the output frequency. For example, if you would like to generate 32 snapshot per NBODY time unit, you could set ``KZ(47)=5``, since 2^5=32.

The simulation data will be stored in the file ``data.h5part``, which can be visualized directly with Paraview using the h5part reader.

Note that HDF5 output facilities is now included in NBODY6++GPU, but this is a special version with the output data optimized for simulating planetary systems in star clusters.
