Virtual environment with `conda`

```
conda create --name deeplearning python=3.9 numpy plotly gdal matplotlib rasterio
conda install -n deeplearning -c conda-forge notebook earthpy pyrosar
```
Alternative (`gdal`, `matplotlib`, `numpy`, `rasterio` implicitly installed as `earthpy` dependencies)
```
conda create --name deeplearning
conda install -n deeplearning -c conda-forge earthpy=0.9.4 notebook pyrosar
conda install -n deeplearning plotly 
```
