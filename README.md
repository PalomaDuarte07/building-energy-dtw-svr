# building-energy-dtw-svr
Reproducible materials for building energy consumption forecasting using SVR and Dynamic Time Warping.

## Reproduction

The experiments in this repository are implemented in the notebook
`notebooks/building_energy_consumption_forecasting.ipynb`.

The DTW-based experiments select one target day from each month. For
each target day, the 12 historical days with the smallest Dynamic Time
Warping (DTW) distance are selected as training samples. The selected
days are then used to train an SVR model, while the target day is used
for evaluation.

Because the target days are randomly selected in the notebook, different
executions may produce different target days and, consequently, different
metrics. To facilitate exact reproduction of the results reported in
the associated study, the target days used in the recorded experiment
are provided below.

Researchers may use these same target days when reproducing the reported
results. Alternatively, different target days may be selected by
following the procedure implemented in the notebook; in this case,
different performance values are expected.

### Office Dawn

| Month | Target day |
|---|---|
| January | 2010-01-11 |
| February | 2010-02-18 |
| March | 2010-03-01 |
| April | 2010-04-24 |
| May | 2010-05-16 |
| June | 2010-06-04 |
| July | 2010-07-25 |
| August | 2010-08-30 |
| September | 2010-09-19 |
| October | 2010-10-14 |
| November | 2010-11-22 |
| December | 2010-12-27 |

### UnivDorm Malachi

| Month | Target day |
|---|---|
| January | 2015-01-31 |
| February | 2015-02-21 |
| March | 2015-03-28 |
| April | 2015-04-06 |
| May | 2014-05-08 |
| June | 2014-06-28 |
| July | 2014-07-29 |
| August | 2014-08-03 |
| September | 2014-09-07 |
| October | 2014-10-23 |
| November | 2014-11-10 |
| December | 2014-12-22 |

### Recorded DTW results

The following values correspond to the target days listed above.

#### Office Dawn

| Target day | RMSE | MAE |
|---|---:|---:|
| 2010-01-11 | 69.5706 | 57.1533 |
| 2010-02-18 | 80.0384 | 69.6170 |
| 2010-03-01 | 80.3308 | 75.0116 |
| 2010-04-24 | 67.6428 | 56.4116 |
| 2010-05-16 | 54.9530 | 47.4303 |
| 2010-06-04 | 42.4096 | 32.5436 |
| 2010-07-25 | 26.0958 | 20.7088 |
| 2010-08-30 | 41.4771 | 31.7408 |
| 2010-09-19 | 34.9608 | 32.1897 |
| 2010-10-14 | 42.7359 | 36.2204 |
| 2010-11-22 | 72.7332 | 58.0636 |
| 2010-12-27 | 64.8307 | 50.1834 |

Mean RMSE: **56.4816**  
Mean MAE: **47.2728**  
RMSE standard deviation: **17.6878**  
MAE standard deviation: **16.0423**

#### UnivDorm Malachi

| Target day | RMSE | MAE |
|---|---:|---:|
| 2015-01-31 | 14.0937 | 10.7433 |
| 2015-02-21 | 6.4008 | 5.0509 |
| 2015-03-28 | 7.9557 | 6.8435 |
| 2015-04-06 | 10.3036 | 8.9503 |
| 2014-05-08 | 9.0902 | 7.8257 |
| 2014-06-28 | 3.2072 | 2.8748 |
| 2014-07-29 | 3.6526 | 3.0052 |
| 2014-08-03 | 2.4061 | 1.8383 |
| 2014-09-07 | 29.1994 | 25.9500 |
| 2014-10-23 | 10.4054 | 7.8161 |
| 2014-11-10 | 11.7324 | 10.4036 |
| 2014-12-22 | 16.5003 | 15.9574 |

Mean RMSE: **10.4123**  
Mean MAE: **8.9383**  
RMSE standard deviation: **7.0173**  
MAE standard deviation: **6.3800**
