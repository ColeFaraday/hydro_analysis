hydro_analysis
==============

Analyze the hydrodynamic evolution file

* SurfaceFinder class use Cornelius algorithm to find iso-thermal hyper-surface
in the hydrodynamic medium. Cornelius is developed and written by Pasi Huovinen
and Hannah Peterson. It is an open source code through OSCAR project. The project
webpage can be found at https://karman.physics.purdue.edu/OSCAR/index.php/CORNELIUS.
The copyright of this subroutine can be found there.

* FluidcellStatistic class include various kinds of flow analysis for the hydrodynamic
medium, including compute the evolution of the flow velocity, spatial eccentricity,
momentum anisotropy, Knudsen and inverse Reynold's number for hydrodynamic fluid cells.

* Hydroinfo_MUSIC class is added to support read in hydrodynamic evolution from 
MUSIC outputs.

To do:
* add cmake compile files


# Usage (Cole)

Note that on Windows one must first install [WSL](https://learn.microsoft.com/en-us/windows/wsl/install) to run the bash scripts.

1. Copy template_hydro and rename suitably
2. Copy the output of [iebe-MUSIC](https://github.com/chunshen1987/iEBE-MUSIC) into `./results/`
3. Change `./parameters.dat` for suitable grid spacing
4. Run `process_multievent_data <IEBE MUSIC FOLDER NAME>`