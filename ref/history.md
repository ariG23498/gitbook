# History Reference

## wandb.sdk.wandb\_history

[\[source\]](https://github.com/wandb/client/blob/21787ccda9c60578fcf0c7f7b0d06c887b48a343/wandb/sdk/wandb_history.py#L3)

History tracks logged data over time. To use history from your script, call wandb.log\({"key": value}\) at a single time step or multiple times in your training loop. This generates a time series of saved scalars or media that is saved to history.

In the UI, if you log a scalar at multiple timesteps W&B will render these history metrics as line plots by default. If you log a single value in history, compare across runs with a bar chart.

It's often useful to track a full time series as well as a single summary value. For example, accuracy at every step in History and best accuracy in Summary. By default, Summary is set to the final value of History.

### History Objects

```python
class History(object)
```

[\[source\]](https://github.com/wandb/client/blob/21787ccda9c60578fcf0c7f7b0d06c887b48a343/wandb/sdk/wandb_history.py#L23)

Time series data for Runs. This is essentially a list of dicts where each dict is a set of summary statistics logged.

