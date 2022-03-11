# Gravity data for doing the homework

The `australia_gravity.csv` file contains a set of gravity observations over
Alice Spings, Australia.
The data points where obtained through a block-reduction of a large compilation
of gravity observations over Australia (Wynne, 2018; Uieda, 2021).
The original dataset is available in
[10.6084/m9.figshare.13643837](https://doi.com/10.6084/m9.figshare.13643837)
under a [Creative Commons Attribution 4.0 International
license](https://creativecommons.org/licenses/by/4.0/).
while the instructions to download and load it using Pooch are in
https://github.com/compgeolab/australia-gravity-data.

The `_prepare_australia_data.ipynb` notebook downloads the original dataset,
crops it to the Alice Springs region and block reduce the data points using
blocks of 5 arc minutes.
It finally stores the resulting observations in the `australia_gravity.csv`
file.


## How to download

You can easily download and load this data file using
[Pooch](https://www.fatiando.org/pooch) and [Pandas]():

```python
import pooch
import pandas as pd

gravity_path = pooch.retrieve(
    url=" https://raw.githubusercontent.com/santisoler/coco-fatiando-tutorial/homework/homework_data/australia_gravity.csv",
    known_hash="sha256:b0f44e5b523a3ca034d07820022c23e5b65875956a88e6eda4cd69f9b66da9fc",
)

data = pd.read_csv(gravity_path)
```


## Citations

- Wynne, P. (2018). NetCDF Ground Gravity Point Surveys Collection (Version
  1.0). Commonwealth of Australia (Geoscience Australia).
  https://doi.org/10.26186/5C1987FA17078
- Uieda, L. (2021). Ground gravity data compilation for Australia version 2.0.
  figshare. https://doi.org/10.6084/m9.figshare.13643837
