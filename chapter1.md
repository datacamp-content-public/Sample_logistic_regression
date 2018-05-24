---
title: Linear regression in classification, why not?
description: >-
  


---
## What is classification?

```yaml
type: NormalExercise

xp: 100

key: fc586953d2
```


 - It is a central topic in machine learning that has to do with teaching machines how to group together data by particular criteria. 
 - It is the process where computers group data together based on predetermined characteristics. 
 - There is an unsupervised version of classification, called clustering where computers find shared characteristics by which to group data when categories are not specified (we will encounter it later, not in this concept).
 - A common example of classification comes with detecting spam emails. 

`@instructions`


`@hint`











---
## Intuition using dummy dataset

```yaml
type: NormalExercise

xp: 100

key: 9647e28718
```

- Let's try and gain some intuition
 - The graph on the next slide depicts if a patient's Tumor is Malignant (Cancerous) or not **{1: Yes; 0: No}** 
 based on the Tumor Size present in his/her body.
 - Tumor Size is taken on the *x-axis* whereas the outcome, i.e., whether the patient's Tumor is Malginant or not is taken on the *Y-axis*
 - The output, "y" has two **categories** i.e. 1 (Yes) or 0 (No) 
 - Therefore, this is a **Classification Problem** where we are using our dependent variables, in this case Tumor Size, and are getting a **binary** output, 1 (Yes) or 0 (No)! 
 - Let's approach this problem with what we've learnt so far i.e. Linear Regression.

Try to plot the tumor dataset created in the codeblock

`@instructions`


`@hint`



`@sample_code`
```{python}
import numpy as np
import matplotlib.pyplot as plt
# import seaborn as sns
import pandas as pd
from sklearn.datasets import make_classification
X, y = make_classification(n_samples=10, n_features=1, n_informative=1, n_redundant=0 , n_clusters_per_class=1, flip_y=0, random_state=7)
```
`@solution`
```{python}
plt.figure(figsize=(10,6))
plt.scatter(X, y, c='r', marker='x')
plt.ylabel("Malignant Tumor {1: Yes  0: No}")
plt.xlabel("Tumor Size")
plt.show()
```






---
## Decision Boundary

```yaml
type: NormalExercise

xp: 100

key: c1fdc0838d
```

* We have fitted a linear regression model which is represented by the blue line
* To convert a continuous output into a discrete one we will be using a threshold value for the output.
* Our output is either 1 or 0, and since we can even get predicted values between 0 and 1 like 0.2, 0.6, etc. (The regression line), we need to come up with a method where our output (0.2, 0.6, etc) is **transformed** to either **0** or **1**, keeping threshold at 0.5
* So, if our predicted value (y) is **greater than 0.5** then we assign a **"1"** to it 
* If y is **less than 0.5** then we assign a **"0"** to it
* Tracing the line of y = 0.5 all the way to it's corresponding x - value (See graph below) we can get to know this "Threshold" value
* This "Threshold Value" is x = __
* This means that if x > _ then y > 0.5 (i.e. y = 1) 
* If x < _ then y < 0.5 (i.e. y = 0)
* Therefore, this vertical line (x = _ ) which separates the 2 classes (y = 1 & 0) ---> **Decision Boundary**

`@instructions`


`@hint`









