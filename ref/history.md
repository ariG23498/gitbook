# History

## wandb.sdk.wandb\_history

[\[view\_source\]](https://github.com/wandb/client/blob/1d91d968ba0274736fc232dcb1a87a878142891d/wandb/sdk/wandb_history.py#L3)

History tracks logged data over time. To use history from your script, call wandb.log\({"key": value}\) at a single time step or multiple times in your training loop. This generates a time series of saved scalars or media that is saved to history.

In the UI, if you log a scalar at multiple timesteps W&B will render these history metrics as line plots by default. If you log a single value in history, compare across runs with a bar chart.

It's often useful to track a full time series as well as a single summary value. For example, accuracy at every step in History and best accuracy in Summary. By default, Summary is set to the final value of History.

### History Objects

```python
class History(object)
```

[\[view\_source\]](https://github.com/wandb/client/blob/1d91d968ba0274736fc232dcb1a87a878142891d/wandb/sdk/wandb_history.py#L23)

Time series data for Runs. This is essentially a list of dicts where each dict is a set of summary statistics logged.

