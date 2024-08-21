# Movie Recommendation System

This project implements a content-based movie recommendation system using the TMDB 5000 Movie Dataset. The system suggests movies similar to a given movie based on various features like genres, keywords, cast, crew, and an overview of the movie.

## Features

- **Data Processing**: The dataset is cleaned and preprocessed to extract relevant features such as genres, keywords, cast, and crew.
- **Feature Engineering**: 
  - The genres, keywords, cast, and crew columns are converted into a list of strings.
  - A new 'tags' column is created by combining the movie overview, genres, keywords, cast, and crew.
- **Text Vectorization**: The 'tags' column is vectorized using `CountVectorizer` to convert the text into a matrix of token counts.
- **Similarity Calculation**: The cosine similarity between the vectorized tags is calculated to measure the similarity between movies.
- **Recommendation**: The system recommends the top 5 movies similar to a given movie.

## Usage

1. **Data Loading**: The project uses the TMDB 5000 Movie Dataset. Ensure the dataset is placed in the `../input/` directory.
2. **Preprocessing**: The dataset is preprocessed to create the 'tags' feature.
3. **Modeling**: Cosine similarity is used to compute the similarity between movies.
4. **Recommendations**: Given a movie name, the system will recommend 5 similar movies.

## Dependencies

- Python 3
- pandas
- numpy
- scikit-learn
- ast
- pickle

## How to Run

1. Clone the repository.
2. Place the TMDB 5000 Movie Dataset in the `../input/` directory.
3. Run the Jupyter notebook or script to build the model and generate recommendations.
4. Use the `recommend(movie_name)` function to get movie recommendations.

## Example

To get recommendations for the movie "Gandhi", you would run:

```python
recommend('Gandhi')

