# Repository for Swiss Cosmo Hackathon

Below organization details and data access.

**Many thanks to everyone who contributed data and code for this hack!**

Credits to most of the repo goes to people including *Leander Thiele*.

## Organization

See here: https://saladino93.github.io/hackathon_unige_2024.html

## Link for presentation slides

https://docs.google.com/presentation/d/1s_ES1H8186SfwJQ613htYLa7YLM8h5aeZ2etjwNion0/edit?usp=sharing


## Using the data

Here is a potential list of data sources you can use (but you can use whatever suits you).

You might want to use Google Colab and Google Drive to ease sharing data and code with your teammates.

### Data 

* Preliminary Uchuu simulation (credits *Riccardo Seppi*), https://drive.proton.me/urls/YNNYYCCJ74#9XTtQrgJmRBo
* Planck Legacy Archive, https://pla.esac.esa.int/#home
* Planck PR4 CMB maps, https://data.cmb-s4.org/planck_pr4.html
* Planck CMB lensing maps, https://github.com/carronj/planck_PR4_lensing
* DES Y3 data, https://des.ncsa.illinois.edu/
* eRosita DR1, https://erosita.mpe.mpg.de/dr1/
* DESI Early Data Release, https://data.desi.lbl.gov/doc/
* Camels simulations, https://camels.readthedocs.io/en/latest/ 
* Websky simulations, https://mocks.cita.utoronto.ca/data/websky/v0.0/
* Half Dome simulations, https://halfdomesims.github.io/
* Quijote simulations, https://quijote-simulations.readthedocs.io/en/latest/index.html


### Data on Google Drive

Data accessible in the [Google drive](https://drive.google.com/drive/u/1/folders/13ySEme-B8XDMYgTZ8_rVpMarRUUGYbTw).

We suggest you use Google colab for the hack, but you decide your best way to work.

It is most straightforward to directly work with the above Google drive from colab,
since the files don't need to leave Google's servers in that case.
The way I figured out how to do this is as follows (there might be a better method):
1. open the above Google drive.
2. right-click on the file or folder you need.
3. click "Organize" -> "Add shortcut".
4. in "All locations", choose "My Drive" and click "Add".
5. in the colab instance, open the "Files" explorer on the left.
6. click "Mount Drive" icon.
7. you should be able to see the file now.
   To switch the colab working directory to your drive, type:
   ``cd "/content/drive/MyDrive/"``


## Available data sets

* **SDSS spectra** (thanks to *Hideki Tanimura*)  
   Some galaxy spectra from the Sloan Digital Sky Survey.  
   loading: [Read\_sdss.ipynb](Read_sdss.ipynb)  
   data: ``sdss_galaxy_spec.hdf5``
* **Gaia** (thanks to *Hideki Tanimura*)  
   Spectra from the Gaia satellite.  
   loading: [Read\_gaia.ipynb](Read_gaia.ipynb)  
   data: ``gaia_star_spec.hdf5``
* **HSC Y1 convergence maps and summary statistics** (thanks to *Joaquin Armijo*)  
   Real and simulated weak lensing convergence maps for HSC Y1.  
   Also available are some summary statistics for these maps.  
   [Marques et al 2023](https://ui.adsabs.harvard.edu/abs/2024MNRAS.tmp...91M/abstract)  
   loading: [HSC\_NG\_ConvergenceMaps.ipynb](HSC_NG_ConvergenceMaps.ipynb)  
   data: ``HSC_NG/``
* **JWST COSMOS web galaxy images** (thanks to *Xuheng Ding*)  
   A sample of galaxy images from JWST.  
   loading: [read\_data\_jwst\_cosmos\_web.py](read_data_jwst_cosmos_web.py)  
   data: ``COSMOS_web_galaxies.zip``
* **HSC images** (thanks to *Chris Nagele*)  
   A sample of galaxy images from HSC.  
   [Nagele et al 2023](https://ui.adsabs.harvard.edu/abs/2023ApJ...947...30N/abstract)  
   loading: [QSO\_SFG\_example.py](QSO_SFG_example.py)  
   data: ``QSO_SFG_data.npy``
* **SIMBIG galaxy catalogs** (thanks to *Bruno Regaldo*)  
   Real and simulated data for SDSS BOSS.  
   Note that the files require [nbodykit](https://nbodykit.readthedocs.io) and [bigfile](https://github.com/rainwoodman/bigfile).  
   [Hahn et al 2023a](https://ui.adsabs.harvard.edu/abs/2023PNAS..12018810H/abstract),
   [Hahn et al 2023b](https://ui.adsabs.harvard.edu/abs/2023JCAP...04..010H/abstract)  
   loading: [simbig\_code/](simbig_code)  
   data: ``simbig_sample.zip``
* **CAMELS 2D multifield data** (thanks to *Francisco Villaescusa-Navarro*)  
   Images of 25 Mpc/h simulated boxes from the [CAMELS](https://camels.readthedocs.io) project.  
   [data website](https://camels-multifield-dataset.readthedocs.io),
   [Villaescusa-Navarro et al 2022](https://ui.adsabs.harvard.edu/abs/2022ApJS..259...61V/abstract)  
   loading: [read\_camels.py](read_camels.py)  
   data: ``CAMELS_multifield``
* **Effective training and upscaling LLMs** (thanks to *Chanjun Park*)  
   This is a special topic run by Chanjun Park.  
   [model on huggingface](https://huggingface.co/upstage/SOLAR-10.7B-v1.0)
* **LLM applied to astro papers** (thanks to *Adam Zadrozny*)  
   Use LLM to extract knowledge from the astro literature.  
   data & code: ``Astro_Papers/``