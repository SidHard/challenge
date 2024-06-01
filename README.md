# WinInternVL

Model Type: Classification

## Description

We use InternVL-14B-224px instead of clip model.

## Setup up python env
- `conda create --name eval python=3.10`
- `conda activate eval`
- `pip install -r requirements.txt`

## Install anomalib
`git clone https://github.com/openvinotoolkit/anomalib`
`cd anomalib && git checkout feature/mvtec-loco && pip install -e .`

## RUN evaluation
Unzip the eval.zip and then
`cd eval`
`CUDA_VISIBLE_DEVICES=0 python evaluation.py --module_path model --class_name MyModel  --dataset_path data/ --mode intervnvl --category juice_bottle`

the pretrain model of InternVL-14B-224px will download from huggingface.
