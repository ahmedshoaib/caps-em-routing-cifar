# Matrix Capsules with EM Routing
A PyTorch implementation of [Matrix Capsules with EM Routing](https://openreview.net/pdf?id=HJWLfGWRb)

## Usage
1. Install [PyTorch](http://pytorch.org/)

2. Start training (default: CIFAR-10)
```bash
python train.py --batch-size 20 --test-batch-size 20
```


## CIFAR-10 experiments

The experiments are conducted on Tesla K80
Specific setting is `lr=0.01`, `batch_size=20`, `weight_decay=0`, Adam optimizer, without data augmentation.

Following is the result after training:

| Arch | EM-Iters | Coord Add | Loss | Epochs | Test Accuracy |
| ---- |:-----:|:---------:|:----:|:--:|:-------------:|
| A=B=C=D=32        | 2 | Y | Spread    | 10 |  62.480   |
| A=64 B=8 C=16 D=16        | 2 | Y | Spread    | 10 |  60.17000   |
| A=32 B=24 C=32 D=24        | 2 | Y | Spread    | 35 |  70.1100   |
| A=B=C=D=32        | 2 | Y | Spread    | 35 |  71.16000   |
| A=64 B=8 C=16 D=16        | 2 | Y | Spread    | 35 |  71.5200   |




## Reference
- https://github.com/shzygmyx/Matrix-Capsules-pytorch
- https://github.com/www0wwwjs1/Matrix-Capsules-EM-Tensorflow
- https://github.com/gyang274/capsulesEM
- https://github.com/yl-1993/Matrix-Capsules-EM-PyTorch
