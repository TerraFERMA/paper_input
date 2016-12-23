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
* ridge
```
cd ridge
tfsimulationharness --run ridgemodel.shml
```
* parallel scaling

```
cd busse_parallel
tfsimulationharness --test busse.shml
```
Note that the parallel scaling test requires editting before running.  It is currently set to run from 1 to 128 processes (so is not
recommended on a desktop).  Additionally, its highest resolution (ncells=64) has > 5 million dofs (also not recommended on a desktop).


