# Spotify Location-Based Playlist Project

This project utilizes geographic coordinates to generate location-based data, integrates with Spotify's API to create personalized playlists, and leverages OpenCage's geolocation API for location information. The project demonstrates combining data from different APIs to create an interactive music experience based on specific geographic locations. 

[TOC]



### Features

- **Geolocation Lookup**: Uses OpenCage API to convert coordinates (latitude, longitude) to human-readable location details such as city and country.
- **Spotify Integration**: Integrates with Spotify using Spotipy library for OAuth authentication to access user playlists and create new ones. 
- **Processing**: Reads and processes coordinate data from a CSV file.



### Prerequisites

1. To set up and run this application, you need the following:

- **Python 3.6+**
- **Spotify Developer Account**: Register an app to obtain the `client_id`, `client_secret`, and `redirect_uri`.
- **OpenCage API Key**: Sign up on OpenCage to obtain an API key for location data.



2. Install the following libraries:

- **requests**: For sending HTTP requests to interact with APIs
- **openai**: (Optional) Integrate with OpenAI's API if needed in future features
- **spotipy**: Spotipy is a lightweight Python library for the Spotify Web API 
- **webbrowser**: Allows opening URLs in a web browser 
- **json**: For handling JSON data from APIs **
- **pandas**: Data manipulation and analysis tool 
- **time**: Used to add delays in request handling, especially useful for rate-limited APIs



3. Install the required Python packages with:

- **Bash**

```bash
pip install requests spotipy pandas
```



### Setup

- **Spotify API Credentials**: In your Spotify Developer Dashboard, create a new app to receive the `client_id`, `client_secret`, and `redirect_uri`.
- **OpenCage API Key**: Place your OpenCage API key in a text file named `OpenCage_key.txt` for secure access.
- **Running the Program**: Run the main script and follow the prompts to input your geographic coordinates and access Spotify's playlist features.

### Usage

- **Input Coordinates**: Launch the application and enter the latitude and longitude of your desired location.
- **Geolocation Lookup**: The app uses OpenCage to retrieve the city and country details associated with the coordinates.
- **Spotify Playlist Creation**: Using Spotify’s API, a playlist is created with the location's name.
- **Playback on Spotify**: Open the playlist on Spotify to start listening.



### Files

- **`spotify_keys.json`**: Contains your Spotify API credentials (`client_id`, `client_secret`, and `redirect_uri`). This file is required for authenticating and accessing Spotify’s API. 
    - **Example Format**:
      ```json
      {
        "client_id": "your_client_id",
        "client_secret": "your_client_secret",
        "redirect_uri": "your_redirect_uri"
      }
      ```

- **`OpenCage_key.txt`**: Stores the OpenCage API key for geolocation queries. Make sure this file is in the same directory as your main script to allow the program to access it.

- **`coordinares.csv`**: A CSV file that contains latitude and longitude data used by the program to look up specific locations. The program reads this file to retrieve the geographic coordinates for playlist generation.



### Example CSV Format

The `coordinares.csv` file should include columns for latitude and longitude. For example:

| latitude | longitude |
| -------- | --------- |
| 40.7128  | -74.0060  |
| 34.0522  | -118.2437 |



### Notes

Ensure all files (`spotify_keys.json`, `OpenCage_key.txt`, and `coordinares.csv`) are in the main project directory for seamless access by the script.