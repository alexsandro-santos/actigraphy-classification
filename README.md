# Actigraphy time series data classification

Based on actigraphy time series data from 96 patients, more than 30 features were extracted. The data were collected through minute-by-minute measurements for 7 days. The patients are classified into 3 groups: "acute insommnia", "chronic insomnia" and "no insomnia". The goal of the project was to train a model that was able to correctly classify patients into these groups.

## Extracted features
| Variable | Name of extracted feature |
| :--- | :--- |
| mean | Mean |
| max | Maximum |
| var | Variance |
| 0.25 | First quartile (25%) |
| 0.5 | Median or second quartile (50%) |
| 0.75 | Third quartile (75%) |
| max_day_n | Maximum of nth day (n=1,..,7) |
| mean_day_n | Mean of nth day (n=1,..,7) |
| var_day_n | Variance of nth day (n=1,..,7) |
| mean_day_var | Variance of daily mean |
| hjorth_mobility | Hjorth mobility |
| hjorth_complexity | Hjorth complexity |
| dfa | Detrended fluctuation analysis |
| pfd | Petrosian fractal dimension |
| permutation_entropy_n_3 | Permutation entropy with n = 3 |
| permutation_entropy_n_4 | Permutation entropy with n = 4 |
| above_f\*max | Value count above f = 70%, 80% and 90% of maximum |
| above_f\*mean | Value count above f = 70%, 80% and 90% of mean |
| above_mean | Value count above mean |
| hfd | Higuchi fractal dimension |
| abs_energy | Absolute energy |
| augmented_dickey_fuller | Augmented Dickey-Fuller |
| cid_ce | Complexity-invariant distance |
| autocorrelation | Autocorrelation |
| fft_centroid | Fast Fourier Transform centroid|
| fft_variance | Fast Fourier Transform variance |
| fft_skew | Fast Fourier Transform skewness |
| fft_kurtosis | Fast Fourier Transform kurtosis |
| kurtosis | Kurtosis |
| skewness | Skewness |
| mean_change | Mean difference of subsequent values |
| mean_2_deriv_central | Mean value of a central approximation of the second derivative |
| interdaily_stability | Interdaily stability (IS) |
| intradaily_variability | Intradaily variability (IV) |

## Main models used
- Quadratic Discriminant Analysis (QDA)
- Multi-Layer Perceptrons (MLP)
- Random Forest

## Note
The package [PyEEG](https://github.com/forrestbao/pyeeg) was used. As it had some problems, it was necessary to place its code inside this repository to correct the problems and use the package.

## Authors
- Alexsandro Santos da Rosa Júnior
- Giovanni Benedetti da Rosa
- Paulo Roberto de Moura Júnior
