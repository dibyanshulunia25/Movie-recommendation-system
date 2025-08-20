# 🎬 Movie Recommendation System with Clustering and Classification

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Pandas](https://img.shields.io/badge/Pandas-1.3+-red)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.2+-orange)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.4+-blueviolet)
![Seaborn](https://img.shields.io/badge/Seaborn-0.12+-lightblue)

A comprehensive movie recommendation system that combines collaborative filtering with machine learning classification to provide personalized movie suggestions. The system clusters users based on their preferences and predicts whether a user will like a movie based on its genre and cluster affiliation.

## 📋 Project Overview

This project analyzes movie rating data to build a sophisticated recommendation system that:
- Clusters users based on their movie preferences
- Predicts whether a user will like a movie using classification algorithms
- Provides personalized movie recommendations based on user clusters
- Visualizes patterns in user preferences and genre popularity

## 📊 Dataset Information

The system uses the MovieLens dataset with the following files:
- `rating.csv`: User ratings for movies (userId, movieId, rating, timestamp)
- `movie.csv`: Movie information (movieId, title, genres)

### Sample Data Structure:
```
   movieId             title                                       genres  userId  rating            timestamp
0        1  Toy Story (1995)  Adventure|Animation|Children|Comedy|Fantasy       3     4.0  1999-12-11 13:36:47
1        1  Toy Story (1995)  Adventure|Animation|Children|Comedy|Fantasy       6     5.0  1997-03-13 17:50:52
```

## 🏗️ System Architecture

The recommendation system follows a multi-stage approach:

1. **Data Preprocessing**: Cleaning and merging datasets
2. **Exploratory Data Analysis**: Understanding rating distributions and genre popularity
3. **User Clustering**: Grouping users based on movie preferences using K-Means
4. **Feature Engineering**: Creating features for classification
5. **Classification Model**: Predicting whether a user will like a movie
6. **Recommendation Engine**: Generating personalized suggestions

## 🔧 Technical Implementation

### Data Processing
- Merged movie and rating datasets
- Handled missing values
- Created genre-based features
- Standardized data for clustering

### User Clustering
- Applied K-Means clustering with 5 clusters
- Used PCA for dimensionality reduction and visualization
- Created user-movie matrix for collaborative filtering

### Classification Model
- Created binary target variable: `liked` (rating ≥ 4)
- Addressed class imbalance using SMOTE
- Trained Random Forest classifier
- Performed hyperparameter tuning with GridSearchCV
- Evaluated model performance using classification metrics

### Key Features:
- **Genre Popularity Analysis**: Visualized most-rated genres
- **User Clustering**: Grouped users with similar preferences
- **Like Prediction**: Binary classification of user preferences
- **Personalized Recommendations**: Cluster-based movie suggestions

## 📈 Results and Visualizations

### Genre Popularity
![Genre Popularity](https://via.placeholder.com/600x400?text=Genre+Popularity+Chart)
*Bar chart showing the most frequently rated genres*

### User Clusters (PCA Projection)
![User Clusters](https://via.placeholder.com/600x400?text=User+Clusters+PCA)
*Visualization of user clusters after dimensionality reduction*

### Ratings Distribution
![Ratings Distribution](https://via.placeholder.com/600x400?text=Ratings+Distribution)
*Histogram showing the distribution of movie ratings*

### Model Performance
- **Accuracy**: 59.0%
- **Precision**: 59% (macro average)
- **Recall**: 59% (macro average)
- **F1-Score**: 59% (macro average)

## 🚀 How to Use the System

### Installation
1. Clone the repository:
```bash
git clone https://github.com/dibyanshulunia25/Movie-recommendation-system.git
cd Movie-recommendation-system
```

2. Install required dependencies:
```bash
pip install -r requirements.txt
```

### Running the Code
1. Ensure the dataset files are in the `archive` folder:
   - `archive/rating.csv`
   - `archive/movie.csv`

2. Execute the Jupyter notebook or Python script:
```bash
jupyter notebook movie_recommendation_system.ipynb
```

### Getting Recommendations
Use the `recommend_movies()` function to get personalized recommendations:
```python
# Get recommendations for user 78
recommendations = recommend_movies(78, num_recommendations=10)
print(recommendations)
```

## 🛠️ Technologies Used

- **Python**: Core programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Scikit-learn**: Machine learning algorithms
- **Matplotlib**: Data visualization
- **Seaborn**: Enhanced visualizations
- **Imbalanced-learn**: Handling class imbalance (SMOTE)

## 📁 Project Structure

```
movie-recommendation-system/
├── archive/
│   ├── rating.csv          # User ratings data
│   └── movie.csv           # Movie information data
├── movie_recommendation_system.ipynb  # Main Jupyter notebook
├── requirements.txt        # Python dependencies
└── README.md              # Project documentation
```

## 🔮 Future Enhancements

- Incorporate more advanced recommendation algorithms (SVD, NMF)
- Add content-based filtering features
- Implement deep learning models for better predictions
- Create a web interface for user interaction
- Expand dataset size for better model training
- Add temporal analysis of user preferences

## 🤝 Contributing

Contributions to improve the recommendation system are welcome. Please feel free to submit issues or pull requests for:
- Bug fixes
- Algorithm improvements
- Additional features
- Documentation enhancements

## 📞 Contact

For questions or suggestions about this project, please contact:
- **Dibyanshu Lunia** - [GitHub Profile](https://github.com/dibyanshulunia25)

## 📚 References

- [MovieLens Dataset](https://grouplens.org/datasets/movielens/)
- [Scikit-learn Documentation](https://scikit-learn.org/stable/)
- [Pandas Documentation](https://pandas.pydata.org/docs/)

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

**Note**: This is a demonstration project for educational purposes. The dataset used is a sample of the full MovieLens dataset for computational efficiency.
