# Emotion-Based-Song-Recommendation
This repo uses the Spotify API and gives us recommendation based on our emotions of any year with the features present in all the songs 
### FEATURES
- Loudness 
- Speechiness 
- Acousticness 
- Instrumentalness 
- Liveness 
- Tempo 
- Valence 
- Energy 
- Danceability
- 
## Functionality has been broken down into 3 parts
1. Mood-based Music Feature Extraction
2. Mood-Based Song Recommender with Spotify API and GUI
3. Spotify Playlist Creator
   
# Mood-based Music Feature Extraction

This script uses the Spotify API (Spotipy) to extract audio features from tracks in different mood-related playlists. The audio features are used to analyze the mood characteristics of the music. The extracted features include loudness, speechiness, acousticness, instrumentalness, liveness, tempo, valence, energy, and danceability.

## Requirements

Make sure you have the following installed:

- Python 3.x
- Spotipy library (`pip install spotipy`)
- Spotify Developer Account and API credentials (CLIENT_ID, CLIENT_SECRET)
- CustomTkinter library (install according to provided instructions)

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

# Mood-Based Song Recommender with Spotify API and GUI

## Overview

This Python application allows you to search for songs based on mood and optionally, the year. It uses the Spotify API to fetch audio features of tracks and match them against predefined mood feature ranges. The user can interact with the application using a graphical user interface (GUI).

## Features

- Mood-based song recommendation: The application matches tracks with predefined mood feature ranges and recommends songs that match the selected mood.
- Optional year selection: You can specify a specific year or allow the application to randomly select one for you.
- User-friendly GUI: The application features a graphical user interface that simplifies user interaction.
- Spotify integration: The application uses the Spotipy library to authenticate and fetch audio features from the Spotify API.


## Setup

1. **Create a Spotify Developer Account:** Register an application on the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/) to obtain your `CLIENT_ID` and `CLIENT_SECRET`.

2. **Configure Redirect URI:** In the code, configure the `REDIRECT_URI` variable. Make sure it matches the redirect URI you provided when registering your Spotify application.

## Usage

1. Run the Python notebook to start the GUI application:

2. The GUI will open. You can choose whether to specify a year or not. Select a mood from the dropdown menu.

3. Click the "SEARCH SONG" button to initiate the song search process.

4. The recommended songs will be displayed in the text box on the GUI interface.

## Disclaimer

This application is for educational and personal use only. It interacts with the Spotify API and adheres to their terms of use. Make sure you comply with Spotify's terms and conditions when using this application.

# Spotify Playlist Creator

This Python script uses the Spotipy library to create a new public Spotify playlist and populate it with songs based on the titles provided in a text file.

## Prerequisites


- Prepare a text file (e.g., `songs.txt`) with a list of song titles, each on a separate line.


## Usage
Open the script (create_playlist.py) and replace the following placeholders with your actual information:

- client_id: Your Spotify Developer application's client ID.
- client_secret: Your Spotify Developer application's client secret.
- username: Your Spotify username.
- playlist_name: The desired name for the playlist.
- file_path: The path to the text file containing song titles.
- Run the script using the following command:
- python create_playlist.py
- The script will create a new public playlist on your Spotify account with the specified name. It will then read the song titles from the text file and search for each song on Spotify. If a match is found, the song will be added t0 the playlist.

## Acknowledgments
- The functionality for extracting music features based on different moods was developed using Python and the Spotipy library. We would like to acknowledge the Spotipy library for providing a straightforward way to interact with the Spotify API programmatically.
  
- The creation of the mood-based song recommender application, which includes a user-friendly GUI, was made possible by combining Python programming with the Spotipy library. We extend our gratitude to the Spotipy library for its role in enabling seamless integration with the Spotify API.
  
- The implementation of the Spotify playlist creation script relied on Python and the Spotipy library. We are grateful for the Spotipy library's capabilities that allowed us to efficiently interact with the Spotify API and automate the process of playlist creation.
