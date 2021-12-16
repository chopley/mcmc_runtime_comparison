### Setup notes

This benchmark uses Jeff Sackmann's tennis data. You can obtain it as follows:

```
git clone https://github.com/JeffSackmann/tennis_atp.git

# If you want to reproduce the results in the blog post, check out this commit:
cd tennis_atp && git checkout 89c20f1ef56f69db1b73b5782671ee85203b068a
```

Here are the steps I followed to setup PyMC v4:

* PyMC v4 installed using the instructions here: https://github.com/pymc-devs/pymc/wiki/Installation-Guide-(Linux)#pymc-v4-installation
* I am running an older version of CUDA (CUDA 10.1), so I couldn't use the
  latest version of JAX. I ended up installing jax v0.2.13 and jaxlib v0.1.65.
* I installed numpyro v0.8.0.
* I installed aeppl version 0.0.17.
