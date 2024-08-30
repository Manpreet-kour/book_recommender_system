Book Recommender System

Overview

This Book Recommender System is a hybrid model that combines popularity-based and collaborative filtering techniques to suggest books to users. The system leverages various libraries, including NumPy, pandas, and scikit-learn's cosine_similarity, to deliver accurate and personalized book recommendations. Users can get similar book recommendations by simply inputting the name of a book.

Features

Hybrid Recommender System: Combines popularity-based filtering with collaborative filtering to improve recommendation quality.

Similarity Function: Uses cosine similarity to find and recommend books similar to a given title.

Top Recommendations: Filters and sorts books based on popularity and average ratings to provide top recommendations.

Dependencies

Python 3.x

NumPy

pandas

scikit-learn

Installation

Clone the repository:



git clone 

Navigate to the project directory:


cd book-recommender-system

Install the required dependencies:


pip install -r requirements.txt

Usage

Load the data: Load your dataset containing book titles, ratings, and other relevant information into a pandas DataFrame.

Popularity-Based Filtering: Filter books with at least 250 ratings and sort them by average rating to get the most popular books:


popular_df = popular_df[popular_df['num_ratings'] >= 250].sort_values('avg_rating', ascending=False).head(50)
Collaborative Filtering: Use the cosine_similarity function to calculate similarity between books based on user ratings:


from sklearn.metrics.pairwise import cosine_similarity

def similarity(book_name):
    # Function logic to return similar books
Get Similar Book Recommendations: Pass a book title to the similarity function to get recommendations:

recommended_books = similarity('Book Title')
print(recommended_books)
