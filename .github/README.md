CPU **compatible** fork of the official SAMv2 implementation.

## Features

* CPU compatible
* Run image and video inference on CPUs
* [Example notebooks](../examples/notebooks/)

## Installation

from the repository:

```bash
pip install git+https://github.com/gaarangoa/samv2.git
```

## Usage

After downloading the official weights, you can use the `load_model()` helper method to instantiate a model.

```python
from sam2 import load_model

model = load_model('../models/tiny', device="cpu")

```

## Citation

```bibtex
@article{ravi2024sam2,
  title={SAM 2: Segment Anything in Images and Videos},
  author={Ravi, Nikhila and Gabeur, Valentin and Hu, Yuan-Ting and Hu, Ronghang and Ryali, Chaitanya and Ma, Tengyu and Khedr, Haitham and R{\"a}dle, Roman and Rolland, Chloe and Gustafson, Laura and Mintun, Eric and Pan, Junting and Alwala, Kalyan Vasudev and Carion, Nicolas and Wu, Chao-Yuan and Girshick, Ross and Doll{\'a}r, Piotr and Feichtenhofer, Christoph},
  journal={arXiv preprint},
  year={2024}
}
```
