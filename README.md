# Clustering Antarctic Penguin Species

![Penguin Image](https://imgur.com/orZWHly.png)

## Project Overview

This project uses unsupervised learning to cluster Antarctic penguins based on various features. The aim is to identify patterns among penguins and potentially uncover the three species known to inhabit the region: **Adelie**, **Chinstrap**, and **Gentoo**. Although the species labels are missing in the dataset, clustering techniques can help reveal natural groupings.

The dataset was sourced from Dr. Kristen Gorman and the Palmer Station, Antarctica LTER, part of the Long Term Ecological Research Network.

## Data Description

The penguin dataset (`penguins.csv`) contains the following columns:

| Column            | Description              |
|-------------------|--------------------------|
| culmen_length_mm   | Bill length (mm)         |
| culmen_depth_mm    | Bill depth (mm)          |
| flipper_length_mm  | Flipper length (mm)      |
| body_mass_g        | Body mass (g)            |
| sex                | Penguin sex (male/female)|

Although species information is unavailable, the features can help us cluster the data into meaningful groups.

## Project Objectives

- Preprocess and clean the dataset for analysis.

- Use clustering (specifically K-Means) to identify clusters in the dataset.

- Visualize the clusters using dimensionality reduction techniques like t-SNE.

- Analyze the average feature values for each cluster to interpret the results.

## Methods

### 1. Data Preprocessing

- **Missing Values**: No missing values were found in the dataset.

- **Categorical Encoding**: The `sex` column was one-hot encoded to convert it into numeric format.

- **Feature Scaling**: All features were standardized using `StandardScaler` to ensure that the K-Means algorithm performs optimally.

### 2. Clustering with K-Means

- **Optimal Cluster Selection**: The Elbow Method was used to identify the optimal number of clusters. Based on the inertia values, the optimal number of clusters was determined to be `4`.

- **Model Training**: K-Means was applied to the scaled data to group the penguins into clusters.

### 3. Visualization

Using t-SNE, the high-dimensional penguin data was reduced to two dimensions for easier visualization. This helps in gaining insights into how well the clustering algorithm has separated the penguins into distinct groups.

### 4. Analysis of Clusters

After clustering, the average feature values for each cluster were calculated, allowing us to interpret the characteristics of each group of penguins.

## Key Results

- **4 Clusters**: The analysis revealed four distinct clusters of penguins based on the selected features.

- **Average Values**: A summary table (`stat_penguins`) shows the average values of the original features for each cluster, offering insight into the potential differences between the penguin species.

## Next Steps and Improvements

- **Species Prediction**: Since we know the penguins likely belong to three species, further analysis can be done to determine whether the clusters align with these species based on known biological characteristics.

- **Dimensionality Reduction**: Try using PCA alongside t-SNE to reduce the dataset's dimensionality and see if it offers a better clustering representation.

- **Cluster Validation**: Explore other clustering algorithms (e.g., DBSCAN or Agglomerative Clustering) to validate the findings and check for consistency.

## Acknowledgments

- **Dataset Source**: Data were collected by Dr. Kristen Gorman and the Palmer Station, Antarctica LTER. A huge thanks to the researchers who made this data publicly available!

- **Penguin Illustration**: Artwork by [Allison Horst](https://github.com/allisonhorst/penguins).
