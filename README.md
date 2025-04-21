🎬 Movie Recommendation System

A content-based recommender engine using NLP and cosine similarity

🌟 Why This Project?
While recommendation systems are common, this implementation:
✔ Handcrafted from scratch (no copy-pasted tutorial code)
✔ Balances accuracy with simplicity – No overkill with deep learning
✔ Explainable – Recommendations are traceable to feature weights

🛠 Tech Stack

-Backend	: Python (Flask), NLP (TF-IDF, NLTK)
-ML Core  : Scikit-learn (cosine similarity)
-Frontend : HTML/CSS/JS (Optional if applicable)
-Data     : TMDB 5000 Movies Dataset

⚙️ How It Works

    Feature Extraction:

        Movie plots/directors/genres → TF-IDF vectors

    Similarity Scoring:

        Cosine similarity compares vectors

    Recommendation:

        Top 5 most similar movies to user input

python

# Simplified core logic  
tfidf = TfidfVectorizer(stop_words='english')  
tfidf_matrix = tfidf.fit_transform(movies['combined_features'])  
cosine_sim = cosine_similarity(tfidf_matrix)  

🚀 Installation
bash

git clone https://github.com/dkour125/mrs.git  
cd mrs  
pip install -r requirements.txt  
python app.py  # Starts Flask server  

📊 What Makes It Unique?

    Custom Weighting: Adjust genre/director/plot importance dynamically

    Interpretable: See why movies were recommended (e.g., "80% genre match")

    Lightweight: <100MB memory usage vs. heavy DL models
http://localhost:8501/
