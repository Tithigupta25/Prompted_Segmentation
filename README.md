**Prompted Segmentation for Crack Detection**

**Overview**

This project uses the Segment Anything Model (SAM) to generate binary segmentation masks for cracks and drywall joints using a prompted segmentation approach. A single point prompt is provided per image, enabling mask generation without manual annotations.

**Datasets**
Cracks-1 (train / validation / test)
Drywall-Join-Detect-1 (train / validation)

**Approach**
SAM with a single center point prompt
Best-confidence mask selected
Binary output:
White (255): defect region
Black (0): background

**Output Structure**
outputs/
 ├── cracks-1/
 │   ├── train_crack/
 │   ├── valid_crack/
 │   └── test_crack/
 └── Drywall-Join-Detect-1/
     ├── train_crack/
     └── valid_crack/

**Installation**
pip install -r requirements.txt
Download SAM checkpoint:
sam_vit_b_01ec64.pth

**Run**
Open and execute:
PromptedSegmentation.ipynb

**Results**
Effective segmentation of thin cracks and wide joints
Consistent performance across datasets
Suitable for pseudo-label generationOverview
