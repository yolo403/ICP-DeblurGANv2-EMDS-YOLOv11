# ICP-DeblurGANv2 & EMDS-YOLOv11: Citrus Flower and Fruit Deblurring Detection

## 📄 Introduction

Accurate detection of citrus flowers and young fruits is an important foundation for early-stage counting and orchard management. To address image blur caused by camera focus inaccuracy and shaking during the acquisition of citrus flowers and young fruits, as well as the challenges of multi-scale features and small-object detection, this study proposes a deblurring detection method that integrates ICP-DeblurGANv2 and EMDS-YOLOv11.

For citrus flower and fruit image deblurring, ICP-DeblurGANv2 adopts FPN-InceptionResNetV2 as the backbone, replaces FPN with PANet to optimize feature fusion, and incorporates CBAM in the PANet head network and lateral connections. For citrus flower and fruit detection, EMDS-YOLOv11 uses EfficientNetV2 as the backbone, adds Multi-Scale Dilated Attention (MSDA) to the small and large object detection heads, improves the original C3k2 module using Dilated With Residual (DWR), and introduces InnerShapeIoU loss to replace CIoU loss.

## 🛠️ Requirements

- Python 3.9
- PyTorch 2.5.1
- CUDA 12.7
- Ultralytics
- `pip install -r requirements.txt`

## 📥 Pre-trained Weights Download

The pre-trained weights for both models are available for download:

- **EMDS-YOLOv11 Weight (`best.pt`)**
  - Link: [Quark Netdisk](https://pan.quark.cn/s/e6e31d13c079)
- **ICP-DeblurGANv2 Weight (`best_fpn.h5`)**
  - Link: [Quark Netdisk](https://pan.quark.cn/s/0bf6b654f0b6)

*Note: Quark Netdisk is recommended for users in China. For international users, please contact the authors for an alternative download link.*

## 📊 Dataset & Reproducibility

- **Original Dataset (ScienceDB):** [https://doi.org/10.57760/sciencedb.014i3](https://doi.org/10.57760/sciencedb.014i3)
- **Data Splits:** `train.txt`, `val.txt`, and `test.txt` are provided in the `data_splits/` folder.
- **Blur Generation:** The synthetic blur generation script is provided as `blur_generation.py` in the repository.
- **Code:** Full source code of both ICP-DeblurGANv2 and EMDS-YOLOv11 is included in this repository.

📧 Contact
For any questions regarding the code, dataset, or pre-trained weights, please contact:
Hang Liu - 15388895367@163.com
