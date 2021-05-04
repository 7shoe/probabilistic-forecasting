# probabilistic-forecasting
A model-agnostic meta library that provides tool for a unified format of probabilistic forecasts, their visualization and assessment.

## Goal
Many (python) libraries provide a wide range of models to predict future values of a time series. Among them, the `scikit-learn`-equivalent `sktime` from the [alan-turing-institue](https://github.com/alan-turing-institute/sktime), `prophet` by [facebook](https://facebook.github.io/prophet/), 
Although they all enable point forecasting (i.e. returning a scalar value for a future unkown measurement) only few of them provide probabilistic forecasts (e.g. predictive quantiles or density functions). Moreover, none of them provides tools to properly assess the quality (i.e. calibration and sharpness) of such probabilistic forecasts.
This library provides meta functionality for various aformentioned libraries. 
Firstly, it provides unqiue data formats for probabilistic forecasts (e.g. a `pd.DataFrame` format for predictive quantiles).
Secondly, various tools to visualize probabilistic forecasts are provided.
Thridly, a comprehensive set of tools to assess calibration and sharpenss is provided, ultimately allowing the researcher/forecaster to decide on the best model. 

## Concepts
Probabilistic forecasts can be provided either as predictive quantiles, predictive density functions or predictive cummulative distribution functions (CDFs).
While point forecasts can be evaluated according to scalar error metrics (e.g. [MSE](https://en.wikipedia.org/wiki/Mean_squared_error), [MAE](https://en.wikipedia.org/wiki/Mean_absolute_error), or [MASE](https://en.wikipedia.org/wiki/Mean_absolute_scaled_error), probabilistic forecasts are, at least technically, infinite dimensional and assessing them requires elaborate functionals .
In recent years, the notions of **calibration** and **sharpness** have dominated. 

## Literature
Probabilistic forecasts are assessed according to their **calibration** and **sharpness**. The cornerstone paper is 
`Probabilistic forecasts, calibration and sharpness` by Gneiting, Balabdaoui, Raftery. [PDF here](https://sites.stat.washington.edu/raftery/Research/PDF/Gneiting2007jrssb.pdf).
