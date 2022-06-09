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

On Linux. The order is important because `-c conda-forge notebook` will update torch packages if it is installed last and effectively break cuda for use in training.
```
conda create -n torch && conda activate torch
conda install -c conda-forge rasterio fiona matplotlib earthpy notebook
conda install -c pytorch pytorch torchvision cudatoolkit=11.3
```

