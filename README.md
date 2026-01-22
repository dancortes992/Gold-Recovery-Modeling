# Gold-Recovery-Modeling
### Background

This project is part of the Tripleten data science practium. Focuses of the project is machine learning.

## Project Description

This project on behalf of Zyfra is tasked with developing a model capable of predicting the amount of gold recovered from gold ore, based on purification data. The model will help to optimize production and eliminate parameters that might be hindering gold recovery in the current process.
To achive this study observered changes in concentrations of metals **(Au, Ag, Pb)** depending on the purification stage. Conducted feed particle size distributions between provided datasets. Considered total concentrations of all substances at different stages.

## Data

Provided data consists of three data sets for gold aquisitions which underwent the purification process; a source dataset, one training and one test set. Features available in the data sets indicate input and output variables of the purification process such as:

 - Metals input feed size particles
 - Output concentrate and tail data for all purification stages.
 - Air levels during process.
 - Chemical activator levels during process.

Our targets for this study are **final.output.recovery** and **rougher.output.recovery** which describe the final and rougher outputs in gold recovery during the process.

**Models evaluated:** RandomForestRegressor, LinearRegression

## Findings

Linear regression model yields best results with an sMAPE of 12.94% on test set. Results found abnormal values of such as:

- zero values present in output of gold during purification
- outlier values in feed particle size.

Removing these abnormalities did in fact lower sMAPE and improve model. Further study is warranted to understand how these "zero values" are appearing as output during purfication.
However based on results, improved consistency of feed particle size input not exceeding majority or minority distribution ranges (avoiding outliers), should lead to higher gold recovery.

## Software

**Tools:** _python_, _jupyter_

**Libraries:** _pandas_, _scipy_, _sklearn_
