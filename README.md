# Discovering-DBSCAN-Intuitive-Guide-to-Density-Based-Clustering-

Here is a much simpler `README.md` matching your actual filenames and without a `requirements.txt`.

```markdown
# Discovering DBSCAN: Intuitive Guide to Density‑Based Clustering

This repository contains a small machine‑learning project that explains the DBSCAN clustering algorithm using:

- A synthetic 2D dataset (`make_circles`) for intuition.
- The real **Mall Customers** dataset (`Mall_Customers.csv`) for practical customer segmentation.

The project was created for a university assignment.

---

## Repository structure

```
.
├─ README.md
├─ LICENSE
│
├─ data/
│   └─ Mall_Customers.csv
│
├─ notebooks/
│   └─ Unveiling DBSCAN: A Powerful Density-Based Clustering Technique.ipynb
│
└─ report/
    └─ Discovering DBSCAN Intuitive Guide to Density-Based Clustering.pdf
```

- **Notebook**: full code (data loading, scaling, DBSCAN experiments, k‑distance plot, k‑means comparison, saving figures/CSVs).  
- **Report**: short written tutorial for beginners.  
- **data**: the Mall Customers CSV file from Kaggle.

---

## What the tutorial shows

### Part 1 – `make_circles` (toy data)

- Generate a two‑ring dataset with `sklearn.datasets.make_circles`.  
- Scale the features and run DBSCAN for several `eps` values.  
- Show how changing `eps` changes:
  - number of clusters,
  - number of noise points,
  - silhouette score.
- Pick `eps ≈ 0.25` to correctly find the two ring‑shaped clusters.

### Part 2 – Mall customer segmentation

- Load `data/Mall_Customers.csv` (Annual Income and Spending Score).  
- Visualise customers in income–spending space.  
- Scale the features with `StandardScaler`.  
- Run DBSCAN with an initial guess for `eps`.  
- Use a 5‑nearest‑neighbour **k‑distance plot** to choose a good `eps` range.  
- Test several `eps` values and select `eps = 0.35`, `min_samples = 5`.  
- Compare the final DBSCAN clusters to k‑means with `k = 5`.

DBSCAN finds several meaningful customer groups and marks unusual customers as noise, while k‑means forces every customer into one of five clusters.

---

## How to run the notebook

1. **Clone the repository**

   ```
   git clone https://github.com/gunti0608/unveiling-dbscan-density-based-clustering.git
   cd unveiling-dbscan-density-based-clustering
   ```

2. **Make sure the dataset is present**

   If `data/Mall_Customers.csv` is missing, download it from Kaggle:

   - Dataset: *Mall Customer Segmentation Data* by `vjchoudhary7`  
     https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python

   Save the file as:

   ```
   data/Mall_Customers.csv
   ```

3. **Open the notebook**

   Use any Python environment with `numpy`, `pandas`, `matplotlib`, `seaborn`, and `scikit-learn` installed.

   ```
   jupyter notebook "notebooks/Unveiling DBSCAN: A Powerful Density-Based Clustering Technique.ipynb"
   ```

   Run all cells from top to bottom. The notebook will regenerate the figures and CSV files in the `figures/` folder.

---

## Accessibility notes

- Plots use a colourblind‑friendly style and different marker shapes.  
- Legends are moved outside the main plotting area so points are not hidden.  
- The report includes figure captions and suggested alt text so screen‑reader users can follow the main ideas.

---

## Licence

This project is released under the **MIT License** (see `LICENSE`). You may use and adapt the code under the terms of that licence.
```
