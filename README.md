<img src=".github/Detectron2-Logo-Horz.svg" width="300" >

Detectron2 is Facebook AI Research's next generation library
that provides state-of-the-art detection and segmentation algorithms.
It is the successor of
[Detectron](https://github.com/facebookresearch/Detectron/)
and [maskrcnn-benchmark](https://github.com/facebookresearch/maskrcnn-benchmark/).
It supports a number of computer vision research projects and production applications in Facebook.

<div align="center">
  <img src="https://user-images.githubusercontent.com/1381301/66535560-d3422200-eace-11e9-9123-5535d469db19.png"/>
</div>
<br>

## Learn More about Detectron2

* Includes new capabilities such as panoptic segmentation, Densepose, Cascade R-CNN, rotated bounding boxes, PointRend,
  DeepLab, ViTDet, MViTv2 etc.
* Used as a library to support building [research projects](projects/) on top of it.
* Models can be exported to TorchScript format or Caffe2 format for deployment.
* It [trains much faster](https://detectron2.readthedocs.io/notes/benchmarks.html).

See our [blog post](https://ai.meta.com/blog/-detectron2-a-pytorch-based-modular-object-detection-library-/)
to see more demos.
See this [interview](https://ai.meta.com/blog/detectron-everingham-prize/) to learn more about the stories behind detectron2.

## Installation

### 1. Install Visual Studio Build Tools 2019

If you are using CUDA 11.8, you will need to install **Visual Studio Build Tools 2019**. Follow the steps in this video tutorial:

👉 [Visual Studio Build Tools 2019 Installation Video](https://youtu.be/lW_xccf8uFA?si=MoGhn54JHjQYrTk2)

Make sure the **“Desktop development with C++"** workload is installed and that these components are selected:

- MSVC v142 - VS 2019 C++ x64/x86 build tools (v14.29)
- Windows 10 SDK (10.0.19041.0)

Once the installation is complete, **restart your computer**.

**Note (not tested):** If you have the latest CUDA (as per May 2025), try installing **Visual Studio Build Tools 2022** and its **“Desktop development with C++"** workload (with MSVC v143 and Windows 11 SDK).

---

### 2. Create Conda Environment

```bash
conda create -n detectron2_env python=3.10 -y
conda activate detectron2_env
```

---

### 3. Install PyTorch

Ensure the PyTorch version and CUDA version match your system. For example, for CUDA 11.8:

```bash
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
```

---

### 4. Install Other Dependencies

```bash
pip install opencv-python pycocotools matplotlib tqdm
```

---

### 5. Install Detectron2 (Windows Build)

```bash
git clone https://github.com/ainhoaarnaiz/detectron2_for_windows.git
cd detectron2_for_windows
pip install -e .
```

---

### 6. Test the Installation (in a Python script)

```python
import detectron2
from detectron2.utils.logger import setup_logger

setup_logger()

# Confirm GPU and detectron2 work
from detectron2.engine import DefaultPredictor
```

## Getting Started

See [Getting Started with Detectron2](https://detectron2.readthedocs.io/tutorials/getting_started.html),
and the [Colab Notebook](https://colab.research.google.com/drive/16jcaJoc6bCFAQ96jDe2HwtXj7BMD_-m5)
to learn about basic usage.

Learn more at our [documentation](https://detectron2.readthedocs.org).
And see [projects/](projects/) for some projects that are built on top of detectron2.

## Model Zoo and Baselines

We provide a large set of baseline results and trained models available for download in the [Detectron2 Model Zoo](MODEL_ZOO.md).

## License

Detectron2 is released under the [Apache 2.0 license](LICENSE).

## Citing Detectron2

If you use Detectron2 in your research or wish to refer to the baseline results published in the [Model Zoo](MODEL_ZOO.md), please use the following BibTeX entry.

```BibTeX
@misc{wu2019detectron2,
  author =       {Yuxin Wu and Alexander Kirillov and Francisco Massa and
                  Wan-Yen Lo and Ross Girshick},
  title =        {Detectron2},
  howpublished = {\url{https://github.com/facebookresearch/detectron2}},
  year =         {2019}
}
```
