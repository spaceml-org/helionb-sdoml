# SpaceML Heliophysics Notebooks: SDO ML
Heliophysics notebooks corresponding to the SDO ML Dataset

## Notebooks:
* **SDO ML Dataset (2018)**
  * In this notebook, we demonstrate the process for interacting with a small sample of the SDO ML dataset. [Galvez, R. *et al* 2019 *ApJS*](https://ui.adsabs.harvard.edu/abs/2019ApJS..242....7G/abstract).
* **Temperature Maps (2018)**
  * Demonstrate a deep-learning approach to differential emission measure inversion using a 1x1 Convolutional Neural Network. [Wright, P. *et al* 2019 *Zenodo*](https://ui.adsabs.harvard.edu/abs/2019zndo...2587015W/abstract).
* **EVE Virtual Instrument (2018)** 
  * *Under development*, based on the work of [Szenicer, A. *et al* 2019 *Science Advances*](https://ui.adsabs.harvard.edu/abs/2019SciA....5.6548S/abstract).
* **AIA Autocalibration (2019)** 
  * Demonstration of the SDO/AIA autocalibration project, based on the work of [Dos Santos *et al* 2021 *A&A*](https://ui.adsabs.harvard.edu/abs/2021A%26A...648A..53D/abstract).


## Interacting with each notebook:

Each notebook is contained within its own <project> folder, and contains a number of files.

```
.
└── notebooks
    └── <project>
        ├── README.md
        ├── <notebook>-colab.ipynb # A Jupyter notebook designed to be executed on Google Colab.
        ├── <notebook>-dev.ipynb # The corresponding local development version of the colab notebook.
        ├── environment.yml # Conda environment file
        └── requirements.txt # Requirements file

```

For local development, the necessary environment can be created as follows (under the assumption that an anaconda installation exists).

```
cd notebooks/<project>
```

```
conda env create -f environment.yml
conda activate <environment>
```
```
# start the jupyter notebook app
jupyter notebook
```

## Contributions
Contributions are welcome as pull requests to the main branch, and should mirror the stucture of existing projects.
