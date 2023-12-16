# Book Recommendation System

## Introduction

Welcome to the Book Recommendation System! This project utilizes natural language processing (NLP) and machine learning techniques to recommend books based on textual and numeric features. The dataset used in this project is sourced from [Kaggle](https://www.kaggle.com/datasets/abdallahwagih/books-dataset/data), and special thanks to the dataset contributor [Abdallah Wagih](https://www.kaggle.com/abdallahwagih) for making this data available.


## Table of Contents
1. [Libraries Import](#1-libraries-import)
2. [Data Read-In / Summarizing Missing Values](#2-data-read-in--summarizing-missing-values)
3. [Data Preprocessing](#3-data-preprocessing)
4. [Vectorization](#4-so-how-do-this-vectorization-even-work)
5. [Similarity](#5-similarity)
6. [Finding a Similar Match](#6-finding-a-similar-match)
7. [Example: Finding Similar Books](#example-finding-similar-books)
8. [How to Install and Run](#how-to-install-and-run)


## 1. Libraries import
Import the necessary libraries for data manipulation, numerical operations, regular expressions, and machine learning tasks such as vectorization and similarity computation.

## 2. Data Read-In / Summarizing Missing Values
Load the dataset into a DataFrame and examine the count of missing values for each column. The output provides insights into the extent of missing data in different columns.

## 3. Data Preprocessing
Selects relevant text and numeric features for book identification, including authors, categories, description, publishing year, number of pages, and average rating.

## 4. Vectorization
Explains the process of converting textual data into numerical vectors using TF-IDF (Term Frequency-Inverse Document Frequency).

## 5. Similarity
Describes cosine similarity, a measure of similarity between two vectors, and generates a similarity matrix for book vectors.

## 6. Finding Similar Books
Introduces a function to find similar books based on a user-provided title.

## 7. Example: Finding Similar Books
### Using the get_most_similar_books function

```python
# Example: Finding Similar Books
book_title = "Harry Potter and the Sorcerer's Stone"

# Using the get_most_similar_books function
similar_books = get_most_similar_books(book_title, similarity_matrix, df, top_n=5)

# Displaying the result
similar_books_table = similar_books.to_markdown(index=False)
print(f"Similar books to '{book_title}':")
print(similar_books_table)