[TerraFERMA](http://terraferma.github.io) input files for:

* Wilson, Cian R., Spiegelman, Marc, van Keken, Peter E., "TerraFERMA: the Transparent Finite Element Rapid Model Assembler for
multi-physics problems in Earth sciences", G3, submitted

Assuming an installed version of TerraFERMA is available they can be built and run using the instructions in the manuscript or below.

Examples:

* thermal convection (isoviscous)
```
cd thermal_convection/isoviscous
tfbuid convection.tfml
cd build
make
make run
```
* thermal convection (temperature dependent viscosity)
```
cd thermal_convection/Tdepviscosity
tfbuid convection.tfml
cd build
make
make run
```
* magma migration
```
cd magma_migration
tfsimulationharness --test magmawaves.shml
```
* parallel scaling
Note that the parallel scaling test will most likely require editting before running as it currently uses up to 128 processes.
```
cd busse_parallel
tfsimulationharness --test busse_parallel
```


