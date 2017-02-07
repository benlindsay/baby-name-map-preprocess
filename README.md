# Baby Name Map Data Preprocesing

This repo stores the preprocessed data used by an [interactive choropleth](http://www.benjlindsay.com/projects/interactive-d3-map-of-baby-name-popularity/) I made on my website, [benjlindsay.com](http://www.benjlindsay.com).

The raw data, downloaded from Kaggle ([download link](https://www.kaggle.com/kaggle/us-baby-names/downloads/us-baby-names-release-2015-12-18-00-53-48.zip)), were processed in `preprocess.ipynb`, and CSV files for the top 1000 most popular names were written to the `data` folder. `preprocess.ipynb` also generated `namelist.csv` which contains all of those 1000 names along with the upper bound for the colorbar scale for each name. That upper bound is the 95th percentile of the percent of boys or girls for any state in any year that has been given each name. The `state_ids.csv` file is just a helper file to used in the preprocessing to connect state abbreviations to the IDs used in the JSON representation of the US map.

If you clone or download this repo, you can open `map.html` with your browser to play with the map. This html file references the `choro.js` Javascript file, which does all the map stuff. If you do this, make sure to use Safari or some other browser that lets you load local data. Chrome does not allow this.
