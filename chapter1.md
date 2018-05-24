---
title: Linear regression in classification, why not?
description: >-
  


---
## What is a classification problem ?

```yaml
type: NormalExercise

xp: 100

key: 524c8b3b5b
```



`@instructions`


`@hint`











---
## Intuition

```yaml
type: NormalExercise

xp: 100

key: 0a60ba3c44
```



`@instructions`


`@hint`



`@sample_code`
```{python}
import numpy as np
import pandas as pd
%matplotlib inline
from sklearn.datasets import make_classification
X, y = make_classification(n_samples=10, n_features=1, n_informative=1, n_redundant=0 , n_clusters_per_class=1, flip_y=0, random_state=7)

```







---
## Decision Boundary

```yaml
type: NormalExercise

xp: 100

key: abdbd30c01
```



`@instructions`


`@hint`



`@sample_code`
```{python}
print(X)
```





