### Mediglot: Medicine Dataset Analysis  

**Project Overview**  
I explored an medicine dataset, focusing on preprocessing, feature engineering, and clustering to derive meaningful patterns.  

**Key Steps**  

1. **Data Cleaning & Exploration**  
   - Removed duplicates and noise (e.g., currency symbols like *₹*).  
   - Analyzed distributions and relationships in the dataset.  

2. **Feature Engineering**  
   - **Text Embeddings**: Used `SentenceTransformer('all-MiniLM-L6-v2')` for contextual features (description, side effects, interactions).  
   - **Categorical Features**: Applied one-hot encoding to salts and manufacturers (low semantic meaning).  
   - **Numerical Handling**: Normalized prices (Gaussian distribution) and imputed missing values (category-wise/global median).  

3. **Dimensionality Reduction & Clustering**  
   - Combined embeddings and reduced dimensions to 2D with **UMAP**.  
   - Clustered via **KMeans** (252 clusters ≈ subcategories).  
   - **Evaluation**: Sampled the first cluster, achieving *100% alignment* with its subcategory.  

**Future Improvements**  
- Expand evaluation to full dataset.  
- Source additional data for robustness.  
- Test alternative embeddings (e.g., BERT variants).  
- Enhance documentation and 3D visualizations.  
