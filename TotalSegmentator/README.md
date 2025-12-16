# TotalSegmentator Setup and Usage (CPU)

## Environment Setup

```bash
conda create -n myenv python=3.11 -y
```

```bash
conda activate myenv
```

```bash
pip install TotalSegmentator
```

```bash
pip install "numpy<2.0"
```

```bash
pip install jupyter ipykernel
```

```bash
python -m ipykernel install --user --name myenv --display-name "Python 3.11 (myenv)"
```

## Fix GradScaler Import Issue

```bash
sed -i.bak 's/from torch import GradScaler/from torch.cuda.amp import GradScaler/' ~/miniconda3/envs/myenv/lib/python3.11/site-packages/nnunetv2/training/nnUNetTrainer/nnUNetTrainer.py
```

## Run TotalSegmentator

```bash
conda activate myenv
```

## Start Jupyter Lab

```bash
conda activate myenv
```

```bash
jupyter lab
```


