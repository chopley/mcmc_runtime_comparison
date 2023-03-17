# MCMC benchmarks

![ESS](images/ess_values.png)

This code compares Stan, PyMC, and PyMC + JAX numpyro sampler on a model for
tennis. It accompanies the blog post available
[here](https://martiningram.github.io/mcmc-comparison/).

### Setup notes

This benchmark uses Jeff Sackmann's tennis data. You can obtain it as follows:

```
mamba env create -f pymc-v4.3.0.yml 
conda activate pymc-v4.3.0
```

Once these are done, here are the steps I followed to setup PyMC v4 with JAX support:


To run the Stan code, it's best to install `cmdstanpy`. Instructions for
installing it can be found [here](https://mc-stan.org/cmdstanpy/installation.html).

### How to run

It's easiest to run the benchmarks using the `fit_all.sh` script. Make sure to
first edit the `target_dir` variable in it and amend it to a directory that
makes sense for you. All the model runs will be stored in it under
subdirectories.

Once benchmarks have been run, you can analyse the results and make plots using
the `Compare_runtimes.ipynb` notebook.

If you run into any problems, please raise an issue!
