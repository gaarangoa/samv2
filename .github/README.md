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

## Download weights
```bash
wget https://dl.fbaipublicfiles.com/segment_anything_2/072824/sam2_hiera_tiny.pt
wget https://dl.fbaipublicfiles.com/segment_anything_2/072824/sam2_hiera_small.pt
wget https://dl.fbaipublicfiles.com/segment_anything_2/072824/sam2_hiera_base_plus.pt
wget https://dl.fbaipublicfiles.com/segment_anything_2/072824/sam2_hiera_large.pt
```

## Usage

After downloading the official weights, you can use the `load_model()` helper method to instantiate a model.

```python
from sam2 import load_model

model = load_model('../models/tiny', device="cpu")

```

add a ```config.yaml``` file to the path where the models are downloaded with the following information:
```yaml
tiny: 
 checkpoint: sam2_hiera_tiny.pt
 config: sam2_hiera_t.yaml
small: 
 checkpoint: sam2_hiera_small.pt
 config: sam2_hiera_s.yaml
base_plus: 
 checkpoint: sam2_hiera_base_plus.pt
 config: sam2_hiera_b+.yaml
large: 
 checkpoint: sam2_hiera_large.pt
 config: sam2_hiera_l.yaml
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
