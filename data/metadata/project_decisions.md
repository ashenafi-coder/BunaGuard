# dataset cleaning

The original Uganda dataset had 3,322 image files. I cleaned it before training.

what I removed:

- 102 broken files that wouldn't open. list in `uganda_invalid_images.csv`.
- exact duplicates (same image saved under different names). kept one copy.
- one group of images that had two different labels (the same picture was
  marked as leaf rust in one folder and phoma in another). since I can't
  tell which label is right, I dropped that group. details in
  `uganda_label_conflicts.csv`.

after cleaning: 1,808 images.

- healthy: 739
- leaf rust: 616
- phoma: 453
