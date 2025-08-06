# Spotify Song Recommender System

A web-based application that provides personalized song recommendations using content-based, collaborative, and hybrid filtering techniques. Built with Streamlit, this project leverages real Spotify data and machine learning to suggest music tailored to user preferences.

## Features

- **Content-Based Filtering:** Recommends songs similar to a given track based on audio features, tags, and metadata.
- **Collaborative Filtering:** Suggests songs based on user listening history and patterns.
- **Hybrid Recommendations:** Combines both methods for more diverse and accurate suggestions.
- **Interactive Web App:** User-friendly interface to input song and artist, select recommendation type, and adjust diversity.

## Demo

Launch the app and enter a song and artist to receive instant recommendations, complete with Spotify preview links.

## Project Structure

- `app.py`: Main Streamlit app for user interaction and displaying recommendations.
- `content_based_filtering.py`: Implements content-based recommendation logic using feature engineering and similarity scoring.
- `collaborative_filtering.py`: Implements collaborative filtering using user-song interaction matrices.
- `hybrid_recommendations.py`: Combines both methods for hybrid recommendations.
- `data_cleaning.py`: Cleans and prepares raw music data for modeling.
- `data/`: Contains raw and processed datasets.
- `notebooks/`: Jupyter notebooks for EDA and model development.
- `requirements.txt`: Python dependencies.
- `Dockerfile`: Containerization setup for deployment.

## Setup Instructions

1. **Clone the repository:**
   ```bash
   git clone <repo-url>
   cd spotify_recomender_system
   ```
2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
3. **Prepare data:**
   Ensure the required CSV and NPZ files are present in the `data/` directory. Use the provided scripts for data cleaning and transformation if needed.
4. **Run the app:**
   ```bash
   streamlit run app.py
   ```

## Usage

- Enter a song name and artist in the app.
- Choose the number of recommendations and filtering method.
- Adjust the diversity slider for hybrid recommendations.
- View and listen to recommended tracks directly in the app.

## Main Dependencies

- `streamlit`
- `pandas`, `numpy`, `scikit-learn`, `scipy`, `joblib`
- `dask`, `category_encoders`

## Data

- `data/Music Info.csv`: Raw song metadata.
- `data/User Listening History.csv`: User-song interaction data.
- Processed files: `cleaned_data.csv`, `transformed_data.npz`, etc.

## Notebooks

- `notebooks/EDA_Spotify_Dataset.ipynb`: Exploratory data analysis.
- `notebooks/Spotify_Collaborative_Filtering.ipynb`: Collaborative filtering development.
- `notebooks/Spotify_Content_Based_Filtering.ipynb`: Content-based filtering development.

## Deployment

- Use the `Dockerfile` and scripts in `deploy/` for containerized deployment.
- `appspec.yml` for deployment automation.

