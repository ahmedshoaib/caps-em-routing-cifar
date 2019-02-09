# Matrix Capsules with EM Routing
A PyTorch implementation of [Matrix Capsules with EM Routing](https://openreview.net/pdf?id=HJWLfGWRb)

## Usage
1. Install [PyTorch](http://pytorch.org/)

2. Start training (default: CIFAR-10)
```bash
python train.py --batch-size 20 --test-batch-size 20
```

Note that master is upgraded to be compatiable with PyTorch `0.4.0`.
If you want to use the old version of PyTorch, please
```bash
git checkout 0.3.1.post3
```

## CIFAR-10 experiments

The experiments are conducted on Tesla K80
Specific setting is `lr=0.01`, `batch_size=20`, `weight_decay=0`, Adam optimizer, without data augmentation.

Following is the result after 10 epochs training:

| Arch | Iters | Coord Add | Loss | BN | Test Accuracy |
| ---- |:-----:|:---------:|:----:|:--:|:-------------:|
| A=B=C=D=32(color)        | 2 | Y | Spread    | Y |  62.10   |
| A=B=C=D=32(B/W)        | 2 | Y | Spread    | Y |  55.2   |
| A=64 B=8 C=16 D=16 (color)        | 2 | Y | Spread    | Y |  60.17000   |




## Reference
- https://github.com/shzygmyx/Matrix-Capsules-pytorch
- https://github.com/www0wwwjs1/Matrix-Capsules-EM-Tensorflow
- https://github.com/gyang274/capsulesEM
- https://github.com/yl-1993/Matrix-Capsules-EM-PyTorch
