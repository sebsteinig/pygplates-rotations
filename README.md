# pyGPlates python notebooks 

## purpose
Reconstruct paleolocations of present-day locations and shapes across the Phanerozoic. [PyGplates](https://www.gplates.org/docs/pygplates/) allows to use some of the functionality of the GUI [GPlates](https://www.gplates.org/) software within python scripts. This allows scripting to automatically process many different locations and/or time periods. Different [rotation models](http://portal.gplates.org/portal/rotation_models/) can be used and are easily exchangeable. I currently use the [PALEOMAP](https://www.earthbyte.org/paleomap-paleoatlas-for-gplates/) rotation model that is consistent to the Bristol [Scotese simulations](https://cp.copernicus.org/articles/17/1483/2021/) by Paul Valdes. 

## input data
Present-day locations for `pyGPlates_site-reconstructions_example.ipynb` need to be defined in a CSV file (age, modern_lat, modern_lon) as shown in the example file `forcordall.csv`. We also need to specify the location of the chosen plate model files, e.g. 'data/PALEOMAP_Global_Plate_Model' ([download link](https://www.earthbyte.org/paleomap-paleoatlas-for-gplates/)). The PyGPlates package can be installed following the instructions in the official [documentation](https://www.gplates.org/docs/pygplates/pygplates_getting_started#installing-pygplates). Other necessary packages for this repo can be installed using the `conda` environemt specified in `environemnt.yml` (see below).

## output data
Input CSV file will get duplicated to `*_reconstructed` with new columns for the reconstructed `PaleoLat` and `PaleoLon`.

## running the notebooks
Easiest way to run locally is to first download the repo with

```
git clone https://github.com/USERNAME/REPOSITORY
``` 

and then install [conda](https://conda.io/projects/conda/en/latest/index.html) (if not installed already). Then create an environment `env_name` with 

```
conda env create --name env_name --file=environment.yml
``` 

using the `environment.yml` file from this repository to install all necessary python packages. The notebooks can then be run interactively by typing

```
jupyter lab
```

