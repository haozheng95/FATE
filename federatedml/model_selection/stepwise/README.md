# Stepwise

Stepwise is a simple, effective model selection technique. FATE provides stepwise wrapper for heterogeneous linear models. The compatible models are listed below:

- Heterogeneous Logistic Regression
- Heterogeneous Linear Regression
- Heterogeneous Poisson Regression 

Please note that due to lack of loss history, Stepwise does not support multi-host modeling. 

To use stepwise, set 'need_stepwise' to `True` and specify stepwise parameters as desired. Below is an example of stepwise parameter setting in job configuration file.

```json
{
"stepwise_param": {
        "score_name": "AIC",
        "direction": "both",
        "need_stepwise": true,
        "max_step": 3,
        "nvmin": 2,
        "nvmax": 6
      }
}
``` 

For examples of using stepwise with linear models, please refer to [examples](../../../examples/federatedml-1.x-examples/hetero_stepwise). For explanation on each stepwise module parameter, please refer to the comments in stepwise param [file](../../param/stepwise_param.py).