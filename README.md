# 2F2L: Forgettable Federated Linear Learning with Certified Data Removal

This is the PyTorch implementation of 2F2L: Forgettable Federated Linear Learning with Certified Data Removal.

### Pretrained Models
We release our pretrained models, where you can download it by execute
```
gdown 1O_Jxo_Kw1YGFS7ktAykfbdS7yZ--ZCbJ
```

### Environment
This project is based on PyTorch 2.3. We also provide `environment.yml`. You can also refer to the colab notebook for setting up the environmenr using pip.

### Data
All of our data are downloaded from official mnist, cifar10, flowers, domainnet and imagenet websites. For your convenience, we provide our pre-processed data below. Please note that we fully acknowledge the copyrights of the original provider of the data. We only temperarily provide the download link of data here for convenience of the users to reproduce our paper.

```
gdown 1-KnnLQyVsZGQKco6zgSqkAQG21I2or6l
```

### Pretrain
```
python pretrain.py --warmup_batch_size <batch_size> --warmup_lr <warmup_lr> --dataset <dataset> --num_users <number_of_clients>
```
An example is given in the notebook.

### Federated Learning (FLT)
```
python flt.py --lr <fl_lr> --train_epochs <total_epochs_for_fl> --dataset <dataset> --mode mixlinear --remove_idx <client_to_forget> --num_users <number_of_clients>
```
Two example are provided in the notebooks.

### Federated Unlearning (FU)
```
python fedremoval.py --lr <fl_lr> --weight_decay <weight_decay> --num_epochs <fedremoval_epochs> --train_epochs <total_epochs_for_fl> --removal_lr <removal_lr> --dataset mnist --mode mixlinear --remove_idx <client_to_forget> --num_users <number_of_clients>
```
Two example are provided in the notebooks.

## Examples
We provide two colab runnable examples. You can open these two notebooks in colab, where it self-contains environment setup, dataset downloads, federated learning and 2F2L.

|  FL Setting   | Details  |
|  ----  | ----  |
| FL from Scratch (MNIST) | Upload this notebook to colab, then there is a demo with FL and FU. |
| FL-FM (DomainNet)  | Upload this notebook to colab, then there is a demo with FL and FU. |
