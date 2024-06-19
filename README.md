# Project No 4: Item-based Filtering Enhanced by SVD (paper implementation)

## Author
- **Serdar Biçici**

## Project Overview
This project explores the application of Singular Value Decomposition (SVD) for enhancing item-based filtering in recommender systems. SVD is a powerful matrix factorization technique used for dimensionality reduction and data compression, revealing the underlying structure of the original matrix to extract essential features. In this implementation, SVD is combined with neighborhood formation (adjusted cosine similarity) to identify similarities in the user-item matrix and generate recommendations.

## Methodology
1. **Data Cleaning and Pre-processing**: 
   - Used an open-source IMDb dataset.
   - Only included reviewers with more than 20 reviews.
   - Normalized the user-item matrix by filling missing values with row and column averages.

2. **Computing SVD**:
   - Implemented the Power Method for finding dominant eigenvalue and eigenvector pairs.
   - Used deflating technique to reveal additional patterns in the data.
   - Employed GPU-based matrix calculations to reduce processing time significantly.

3. **Neighborhood Formation**:
   - Calculated adjusted cosine similarity for each pair of items after dimensionality reduction.
   - Created a symmetric similarity matrix to identify the most similar items.

4. **Prediction Generation**:
   - Used a weighted sum formula to generate predictions based on item similarities.
   - Applied this method to each item rated by the user to provide top recommendations.

## Experiments and Results
- Conducted several experiments to determine optimal parameters for the most accurate predictions.
- **Optimal k Value**: Found that k=6 gives the best results for pseudo-users.
- **Optimal n Value**: Using k=6, determined the best value for n to be 10 for top recommendations.

## Conclusion
The implementation demonstrates the effectiveness of combining SVD with item-based filtering to enhance recommendation systems. By optimizing the parameters k and n, the system provides accurate and efficient recommendations, showcasing the potential of SVD in handling large datasets and improving data analysis and modeling.

## References
Vozalis, Manolis, and Margaritis, Konstantinos G.. (2005). Applying SVD on item-based filtering. 464-469. 10.1109/ISDA.2005.25.
