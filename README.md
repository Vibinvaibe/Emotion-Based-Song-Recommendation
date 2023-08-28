# Emotion-Based-Song-Recommendation
This repo uses the Spotify API and gives us recommendation based on our emotions of any year with the features present in all the songs (FEATURES-Loudness Speechiness Acousticness Instrumentalness Liveness Tempo Valence Energy Danceability)
# Mood-based Music Feature Extraction

This script uses the Spotify API (Spotipy) to extract audio features from tracks in different mood-related playlists. The audio features are used to analyze the mood characteristics of the music. The extracted features include loudness, speechiness, acousticness, instrumentalness, liveness, tempo, valence, energy, and danceability.

## Requirements

Make sure you have the following installed:

- Python 3.x
- Spotipy library (`pip install spotipy`)
- Spotify Developer Account and API credentials (CLIENT_ID, CLIENT_SECRET)

## Setup

1. Replace `your_client_id` and `your_secret_id` with your actual Spotify API credentials.
2. Set up the desired scopes and redirect URI in the `SCOPE` and `REDIRECT_URI` variables.
3. Run the script in a Python environment that has the required libraries.

## Features Extraction

1. The script authenticates with the Spotify API using OAuth2.
2. It fetches track names from a specified playlist using `get_track_names_from_playlist` function.
3. The `give_features` function extracts audio features from a given track using its name.
4. Various audio features (loudness, speechiness, etc.) are extracted and returned.
5. Features are then scaled to a 0-1 range using scaling functions.

## Range Calculation

1. The `range_calc` function calculates the optimal data range for a given feature within a specified range length.
2. The goal is to capture as many data points as possible within the target range length while covering at least 75% of the data.

## Main Process

1. The script iterates over the extracted song features and applies scaling and range calculation.
2. The feature ranges are then displayed in the format (`min_range`, `max_range`).
3. The script unscales tempo and loudness ranges for better readability.

## Extracted Mood Features

The script includes a dictionary of mood-related features extracted from various playlists. Each mood is associated with specific ranges for different audio features.

## Usage

1. Configure your Spotify API credentials in the script.
2. Run the script.
3. Check the printed feature ranges for different moods.
4. You can use these ranges to classify songs based on mood.

## Disclaimer

Please note that the ranges and mood classifications are based on the specific playlists and tracks used for feature extraction. They might not be representative of all songs within a given mood category.

## References

- Spotify Developer Dashboard: [Link](https://developer.spotify.com/dashboard/applications)
- Spotipy Documentation: [Link](https://spotipy.readthedocs.io/en/2.19.0/)

- # Mood-Based Song Recommender with Spotify API and GUI

## Overview

This Python application allows you to search for songs based on mood and optionally, the year. It uses the Spotify API to fetch audio features of tracks and match them against predefined mood feature ranges. The user can interact with the application using a graphical user interface (GUI).

## Features

- Mood-based song recommendation: The application matches tracks with predefined mood feature ranges and recommends songs that match the selected mood.
- Optional year selection: You can specify a specific year or allow the application to randomly select one for you.
- User-friendly GUI: The application features a graphical user interface that simplifies user interaction.
- Spotify integration: The application uses the Spotipy library to authenticate and fetch audio features from the Spotify API.

## Requirements

- Python 3.x
- Spotipy library (install using `pip install spotipy`)
- CustomTkinter library (install according to provided instructions)

## Setup

1. Clone or download this repository to your local machine.

2. Install the required libraries by running the following commands in your terminal:

   ```bash
   pip install spotipy
   # Install CustomTkinter (provide installation instructions if applicable)

