# Dataset

This folder documents the Ethiopian smartphone coffee-leaf dataset used in the
notebook. Dataset images are not stored in this Git repository. Download the
CC BY 4.0 source dataset from Mendeley Data:
https://doi.org/10.17632/k36wnd6knb.1

Please cite the original dataset authors: Specioza Chelangat, Racheal
Anirwoth, Kizito Najib Mayanja, and Abubakhari Sserwadda (2025), *A Machine
Learning Dataset for Classification of Common Coffee Leaf Diseases in
Uganda*, Mendeley Data, Version 1.

The cleaned dataset has 1,808 images across three classes:

```text
prepared/coffee_leaf_dataset/
|-- healthy/      739 images
|-- leaf_rust/    616 images
`-- phoma/        453 images
```

## Cleaning

The original download contained 3,322 files. I removed 102 unreadable or
corrupted files, exact duplicates, and one duplicate group that appeared
under both the leaf-rust and phoma labels.

The cleaning records are saved in `metadata/uganda_invalid_images.csv`
and `metadata/uganda_label_conflicts.csv`.

## Path in the notebook

The notebook accesses the cleaned dataset with:

```python
DATASET_PATH = PROJECT_ROOT / "data" / "prepared" / "coffee_leaf_dataset"
```
