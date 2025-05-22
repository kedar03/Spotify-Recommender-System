# 🎧 Spotify Recommender System

A content-based music recommendation engine built using a dataset of ~280,000 songs. This system recommends songs similar to those in a user's playlist by analyzing track features, genres, and popularity. Playlist data is fetched using the Spotify API.

---

## 🚀 Overview

This project helps users discover new music by generating 40 similar song recommendations based on the tracks in their Spotify playlist. It uses feature engineering and cosine similarity to compare user playlist tracks with a large dataset of songs.

---

## 🧠 Features

- Connects to Spotify via the **Spotify API** to fetch user playlist details  
- Applies **TF-IDF** vectorization on genres and **one-hot encoding** on year and popularity  
- Uses **cosine similarity** to find and recommend the 40 most similar tracks  
- All logic and implementation are contained in a single notebook: `Recommendations_Final.ipynb`

---

## 🛠️ Tech Stack

- **Language:** Python  
- **Notebook:** Jupyter Notebook (`Recommendations_Final.ipynb`)  
- **Libraries:** Pandas, NumPy, Scikit-learn, Spotipy  
- **Techniques:** TF-IDF, One-Hot Encoding, Cosine Similarity  
- **API:** Spotify Web API

---

## 📊 Dataset

- **Source:** [Kaggle Spotify Dataset](https://www.kaggle.com/datasets)  
- **Size:** ~280,000 songs  
- **Key Columns Used:** `genres`, `popularity`, `year`, `track_id`  
- **Preprocessing:**  
  - One-hot encoding of `year` and `popularity`  
  - TF-IDF vectorization of `genres`  
  - Merging features for similarity calculation

---

## ⚙️ How to Run

1. **Clone the repository**

    ```bash
    git clone https://github.com/your-username/spotify-recommender-system.git
    cd spotify-recommender-system
    ```

2. **Install dependencies**

    ```bash
    pip install -r requirements.txt
    ```

3. **Set up Spotify API credentials**

    - Create an app at the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/)
    - Save your `client_id`, `client_secret`, and `redirect_uri` in the notebook

4. **Open the Jupyter notebook**

    ```bash
    jupyter notebook Recommendations_Final.ipynb
    ```

5. **Provide your Spotify playlist URI** when prompted in the notebook

---

## 📸 Sample Output

| Spotify Playlist (Input) | Recommended Tracks (Output) |
|--------------------------|-----------------------------|
| ![Spotify Playlist](screenshots/Playlist_Snippet.png) | ![Recommended Tracks](screenshots/Recommender_System_Output.png) |

---

## 🧪 Future Improvements

- Improve vectorization by including more track features (e.g., audio features via Spotify)  
- Expand the recommendation engine with collaborative filtering or hybrid models  
- Package into a web app for real-time recommendations

---

