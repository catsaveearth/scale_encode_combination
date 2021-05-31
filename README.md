# scale_encode_combination

## introduction
It helps with scaling &amp; encoding of dataset. </br>
This project belongs to Data science term project, Gachon Univ. ( 2021 spring semester )
<br><br>

## Getting Started
Just clone or download! </br>
Run the function by referring to the test.
<br><br>


## example
```python
import pandas as pd
from Scale_Encode_Combination import scale_encode_combination
from pprint import pprint

# sample dataset (6 row)
dataset = pd.read_csv("sample_datas.csv")

#set numerical feature list
numerical_feature_list = ['duration_ms']

#set categorical feature list
categorical_feature_list = ['time_signature']

# run!
combination_dataset = scale_encode_combination(dataset, numerical_feature_list, categorical_feature_list)

#check result
pprint(combination_dataset)

# [output]
# {'minmax_onehot':    Unnamed: 0  duration_ms  time_signature_1  time_signature_3  time_signature_4  time_signature_5
# 0           1     0.000000                 1                 0                 0                 0
# 1           2     1.000000                 0                 0                 0                 1
# 2           3     0.943277                 0                 1                 0                 0
# 3           4     0.777565                 0                 0                 1                 0
# 4           5     0.967558                 0                 0                 1                 0
# 5           6     0.434648                 0                 0                 0                 1,
#  'minmax_ordinal':    Unnamed: 0  duration_ms  time_signature
# 0           1     0.000000             0.0
# 1           2     1.000000             3.0
# 2           3     0.943277             1.0
# 3           4     0.777565             2.0
# 4           5     0.967558             2.0
# 5           6     0.434648             3.0,
# ....
```
<br><br>

## Sample dataset
This is part of ["Spotify Dataset 1922-2021, ~600k Tracks"](https://www.kaggle.com/yamaerenay/spotify-dataset-19212020-160k-tracks)

