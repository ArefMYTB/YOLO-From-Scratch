# YOLOv8 from Scratch 🚀

This repository implements **YOLOv8 (You Only Look Once v8)** from scratch using **PyTorch**, including the backbone, neck, and head. It also supports training on the **COCO dataset** and includes **Distribution Focal Loss (DFL)**, **Classification Loss**, and **Localization Loss**.

---

## 🧱 Architecture

The architecture is modular and consists of:

### ✅ Backbone
Extracts hierarchical features from input images. Uses:
- `Conv` Blocks
- `C2f` Layers (lightweight bottlenecks)
- `SPPF` (Spatial Pyramid Pooling — Fast)

### ✅ Neck
Fuses features across scales using:
- Top-down and Bottom-up paths
- `C2f` Layers
- `Upsample`, `Downsample`, `Concat`

### ✅ Head
Performs detection at three different scales:
- Multi-scale classification and regression heads
- Outputs include:
  - Classification logits
  - Bounding box bin predictions (via DFL)
  - Decoded boxes during inference
