# TPCx-AI Supplyment

A supplement repo for TPCx-AI benchmark (v1.0.2)

**TPCx-AI_Datagen.sh**

> A script to generate the dataset of TPCx-AI Benchmark

**requirements.txt**, **requirements-ks.txt**

> Third-party Python libs that are needed for virtual environment of TPCx-AI. 

# Setup TPCx-AI Benchmark

## Install Pythen Virtual Environment

According to `setup-python.sh`, we have to conduct two virtual envrionment in `lib` folder with names `python-venv` and `python-venv-ks`. Furthermore, we need to install necessary depencies to these two venv using `requirements.txt` and `requirements-ks.txt`. These two requirements are based on the `python.yaml` and `python-ks.yaml` in the folder `tpcx-ai/tools/python`. 

**However, if we only need to generate data using single node, we can just create `python-venv` and install the dependencies using `pip3 install -r requirements.txt`. Also, we need to install workload and driver by running `pip3 install -e workload/python` and `pip3 install -e driver`.**

**`python-vevn-ks` will be used in phase loading, training, etc**

If we got RuntimeError `CMake must be installed to build the following extensions: dlib`, we need to install `cmake` in the virtual environment by `pip3 install cmake`.

## Generate Dataset

After installing the python virtual environment and the associate depencies, we could run `TPCx-AI_Datagen.sh` to generate the dataset which should be located in the folder `output`.