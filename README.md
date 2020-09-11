# NB

Nenural network Blocks (aka: **NB**, or neural network builder). This library provides massive fancy blocks for you for quick import to build your powerful. Some SOTA tricks and connections such as CSP, ASFF, Attention, BaseConv, Hardswish, all included for quick prototype your model.

**nb** is an idea comes from engineering, we build model with some common blocks, we exploring new ideas with SOTA tricks, but all those thing can be gathered into one single place, and for model quick design and prototyping.

this project is under construct for now, I will update it quickly once I found some new blocks that really works in model. Also, every single updated block will be recorded in updates.



## Usage

Here is an example of using NB to build YoloV5!

```

```

A simple example to build a layer of conv:

```python
from nb.torch.base.conv_block import ConvBase

a = ConvBase(128, 256, 3, 1, 2, norm_cfg=dict(type="BN"), act_cfg=dict(type="Hardswish"))

```
Be note that, the reason for us using `cfg` to specific norm and activation is for users dynamically switch their configuration of model in yaml format rather than hard code it.



## Updates

- **2020.09.12**: New backbone SpineNet added:

  SpineNet is a backbone model specific for detection, it's a backbone but can do FPN's thing!! More info pls reference google's paper [link](https://ai.googleblog.com/2020/06/spinenet-novel-architecture-for-object.html).
  
  ```python
  from nb.torch.bakbones.spinenet import SpineNet
  
  model = SpineNet()
  ```
  
  
  
- **2020.09.11**: New added blocks:

  ```
  resnet.Bottleneck
  resnet.BasicBlock
  
  ConvBase
  ```





## Support Matrix

We list all `conv` and `block` support in **nb** here:

- `conv`:
  - Conv
  - ConvWS: https://arxiv.org/pdf/1903.10520.pdf
  - ...
- `Blocks`:
  - CSPBlock: 
  



## Copyright

@Lucas Jin all rights reserved.