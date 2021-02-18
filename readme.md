# CUDA version
input: \
`/usr/local/cuda/bin/nvcc --version`

output:
```
nvcc: NVIDIA (R) Cuda compiler driver
Copyright (c) 2005-2018 NVIDIA Corporation
Built on Sat_Aug_25_21:08:01_CDT_2018
Cuda compilation tools, release 10.0, V10.0.130
```

Requires `tensorflow-1.15`

# VirtualEnv

Create `venv` with python 3.7.4 - `python3 -m venv venv`

Install `pip` packages - `pip install -r requirements.txt`

Then install additional packages:
```
python -m deeppavlov install squad_bert
ipython kernel install --user --name=.env
jupyter labextension install @jupyter-widgets/jupyterlab-manager
```
Export following variable:\
`export LD_LIBRARY_PATH=/usr/local/cuda-10.0/lib64`

# Clean install

Install following packages:
```
pip install deeppavlov
python -m deeppavlov install squad_bert
pip install tensorflow-gpu==1.15.2

pip install jupyterlab
pip install ipywidgets
ipython kernel install --user --name=.env
jupyter labextension install @jupyter-widgets/jupyterlab-manager

pip install numba
pip install openpyxl

pip install matplotlib
pip install seaborn
```

Export following variable:\
`export LD_LIBRARY_PATH=/usr/local/cuda-10.0/lib64`

You should be good to go :)
