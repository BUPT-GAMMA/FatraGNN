# Official Pytorch implementation of WWW'24 paper "Graph Fairness Learning under Distribution Shifts" 



## Requirements

To install requirements:

```setup
pip install -r requirements.txt
```

## Dataset

Datasets can be found in [https://anonymous.4open.science/r/FatraGNN-118F.](https://github.com/liushiliushi/FatraGNN)

## Training

To train FatraGNN on the five datasets, run these commands:

```train
python fatragnn.py --gpu 3 --ood 2 --dataset=bail --encoder=GCN --inid=_B0 --outid=all --times=config1
python fatragnn.py --gpu 3 --ood 2 --dataset=credit --encoder=GCN --inid=_C0 --outid=all --times=config1
python fatragnn.py --gpu 3 --ood 2 --dataset=pokec --encoder=GCN --inid=_z --outid=all --times=config1
```
Train on sync-B1s and sync-B2s
```train
python fatragnn.py --gpu 3 --ood 1 --dataset=bail --encoder=GCN --inid=_B0 --outid=_md0 --times=config2
python fatragnn.py --gpu 3 --ood 1 --dataset=bail --encoder=GCN --inid=_B0 --outid=_md3 --times=config3
```


