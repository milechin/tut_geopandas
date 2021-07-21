# Introduction to GIS - Using GeoPandas - Conda Environment Setup

1. Clone the git repository: https://github.com/milechin/tut_geopandas.git  
 1. Enter ```tut_geopandas``` directory.  
 3. Download tutorial files from here: http://rcs.bu.edu/examples/gis/tutorials/python_geopandas/tutorial_files.zip  
 4. Unzip the ```tutorial_files.zip``` into ```tut_geopandas/tutorial_files```.  Create the "tutorial_files" directory if needed.
 5. Use the provided ```environment.yml``` file to create the "tut_geopandas" conda environment for the workshop.   
     ```conda env create -f environment.yml```
     
 6. Activate the "tut_geopandas" environment.  
     ``` conda activate tut_geopandas ```
     
 8. Launch jupyter notebook.  
     ```jupyter notebook```
     
 10. Open the ```Intro to GIS - GeoPandas.ipynb``` notebook. (Note: it may complain that the correct kernel is not found, just set "Python3", if available.)
