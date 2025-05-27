# Movie Recommendation System

---

# 🎬 Movie Recommendation System

A content-based movie recommender system built with Python and Streamlit that suggests similar movies based on user input.

## 📌 Project Overview

This system analyzes movie metadata—including genres, keywords, and overviews—to recommend films similar to a selected title. Utilizing natural language processing and machine learning techniques, it provides personalized movie suggestions.

---

## 🚀 Features

* Interactive web interface using Streamlit
* Content-based filtering with TF-IDF vectorization
* Cosine similarity for measuring movie similarity
* Integration with OMDb API to fetch movie posters and plots
* Efficient data preprocessing and caching for performance

---

## 🛠️ Tech Stack

* **Frontend:** Streamlit
* **Backend:** Python
* **Libraries:** Pandas, NumPy, Scikit-learn, NLTK, Requests, Joblib
* **API:** OMDb API

---

## 📂 Project Structure

```

Movie-Recommendation-System/
* ├── app.py
* ├── config.json
* ├── movies.csv
* ├── omdb_utils.py
* ├── preprocess.py
* ├── recommend.py
* ├── df_cleaned.pkl
* ├── tfidf_matrix.pkl
* ├── cosine_sim.pkl
* └── requirements.txt
```

* `app.py`: Main application script for Streamlit
* `config.json`: Configuration file containing the OMDb API key
* `movies.csv`: Dataset containing movie information
* `omdb_utils.py`: Utility functions to fetch movie details from OMDb API
* `preprocess.py`: Script for data cleaning and preprocessing
* `recommend.py`: Contains the recommendation logic
* `df_cleaned.pkl`, `tfidf_matrix.pkl`, `cosine_sim.pkl`: Serialized objects for faster loading
* `requirements.txt`: List of required Python packages

---

## ⚙️ Setup Instructions

1. **Clone the repository:**

   ```bash
   git clone https://github.com/Shibaditya00/Movie-Recommendation-System.git
   cd Movie-Recommendation-System
   ```


2. **Create and activate a virtual environment (optional but recommended):**

   ```bash
   python -m venv venv
   # On Windows
   venv\Scripts\activate
   # On Unix or MacOS
   source venv/bin/activate
   ```


3. **Install the required packages:**

   ```bash
   pip install -r requirements.txt
   ```


4. **Obtain an OMDb API key:**

   * Sign up at [OMDb API](http://www.omdbapi.com/apikey.aspx) to get a free API key.

5. **Configure the API key:**

   * Create a `config.json` file in the root directory with the following content:

     ```json
     {
       "OMDB_API_KEY": "your_api_key_here"
     }
     ```

6. **Preprocess the data:**

   ```bash
   python preprocess.py
   ```


7. **Run the application:**

   ```bash
   streamlit run app.py
   ```

---

## 📊 How It Works

1. **Data Preprocessing:**

   * Combines genres, keywords, and overviews into a single text field.
   * Cleans the text by removing stopwords and punctuation.
   * Applies TF-IDF vectorization to convert text into numerical features.
   * Calculates cosine similarity between movies.([GitHub][9])

2. **Recommendation Logic:**

   * When a user selects a movie, the system finds similar movies based on cosine similarity scores.
   * Fetches additional details like plot and poster from the OMDb API.

---

## **Dataset**

<a href="https://github.com/Shibaditya00/Movie-Recommendation-System/blob/main/src/movies.csv">Movies Dataset</a>

---

## 🖼️ Sample Output

![Screenshot (54)](https://github.com/user-attachments/assets/36a593c2-960d-4022-ab2e-355a21242e03)


![Screenshot (55)](https://github.com/user-attachments/assets/0fb8438d-57f5-4baa-b040-33b602709ca7)


![Screenshot (64)](https://github.com/user-attachments/assets/b52b4be4-fab7-4a61-a18d-239a5136b7fc)


![Screenshot (65)](https://github.com/user-attachments/assets/bb29b94c-28cb-4a65-a753-9d70c188f73b)




---

