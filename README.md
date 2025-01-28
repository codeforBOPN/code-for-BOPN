# BOPN

This repository provides a reference implementation of **BOPN** and pre-trained models as described in the paper:

The code is implemented using **PyTorch**.


## Getting Started

This repository includes codes for solving two combinatorial optimization (CO) problems:

- **Asymmetric Traveling Salesman Problem (ATSP)**
- **Permutation Flow Shop Problem (PFSP)**

## Basic Usage

For both `ATSP_BOPN` and `FFSP_BOPN`, the following steps outline the usage:

### i. Model train
To train a model, run the following command:
```bash
python3 train.py
```
train.py contains parameters you can modify.
At the moment, it is set to train N=20 problems.

### ii. Model test
To test a model, run the following command:
```bash
python3 test.py
```
You can specify the model as a parameter contained in test.py.
At the moment, it is set to use the saved model (N=20) we have provided (in "result" folder), but you can easily use the one you have trained from running train.py.

To test for the N=50 model, make sure that saved problem files exist in the path (see below for Datasets). Also, modify test.py so that

all "20"'s are changed to "50"
"path" and "epoch" in the "tester_params" are correctly pointing to the saved model

## Additional PFSP Description

Unlike ATSP, PFSP must take into account both the number of jobs and the machines in learning and inference.
Generalization experiments are possible for work with the same facilities.
















