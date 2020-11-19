# Long training script for imagenette and woof 

## Original code 

You can find it here: [train_imagenette](https://github.com/fastai/fastai/blob/master/nbs/examples/train_imagenette.py)

## What's added ?

Added support for variants of MixUp

1. Manifold MixUp 

2. CutMix

## Requirements

- fastai >= 2
- manifold_mixup module which you can find here: [ManifoldMixupV2](https://github.com/nestordemeure/ManifoldMixupV2)

## How to use ?

You just pass a tuple to the *mix* argument.

The first element of the tuple will be the type of mix you want (it's a string).

- **'mix'**, for input mix (original MixUp).

- **'manifold'**, for Manifold MixUp.

- **'cut'**, for CutMix.

The second element of the tuple will be the alpha parameter (it's a float).

If you don't want to apply any *mix* pass **None**.

## Note

If you want to know more about these data augmentation techniques, check out my blog post: [Mixup, Manifold Mixup and CutMix](https://igrek-code.github.io/blog/2020/11/18/mixup_manifold_mixup_cutmix.html)
