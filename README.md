# MyMusic User Manual

I created MyMusic to help you export music playlists, organize them efficiently, and enjoy them through a web app with both video and audio playback capabilities. I want to thank the resources that made this project possible, including Claude.ai, GitHub, GitHub Pages, OnRender.com, and SoundCloud.

## Step 1: Exporting Your Spotify Playlist to CSV

### 1. Preparing Your Playlist
First, open your Spotify account and select the playlists you want to export.

### 2. Using TuneMyMusic
I used TuneMyMusic for the export process:
- Go to TuneMyMusic's website
- Select Spotify as your source
- Follow their export instructions to get your playlist in CSV format

The exported CSV includes important song details:
- Title
- Artist Name
- Album Name
- Playlist Name
- Type
- ISRC Code
- Spotify ID

### 3. Cleaning Up the CSV Data
I found that not all exported data was necessary, so I:
- Removed unnecessary columns (Playlist Name, Type, ISRC, Spotify ID)
- Kept only the essential columns: Song Title, Artist Name, and Album Name
- After cleaning, my final list contained 2,965 songs

## Step 2: Extracting Media Links

### 1. Web Scraping with Python
I developed a Python script that:
- Automatically searches YouTube using the Song Title and Album Name
- Extracts the corresponding YouTube links
- Searches SoundCloud for audio versions of the songs
- Collects SoundCloud track IDs and embed codes
- Enables both video and audio playback functionality in the app

### 2. SoundCloud Integration
I implemented SoundCloud support by:
- Using the SoundCloud API to search for tracks
- Storing track IDs for each song when available
- Creating fallback options when songs aren't found on SoundCloud
- Implementing the SoundCloud widget for seamless audio playback

## Step 3: Creating the Web App

### 1. Web App Development
I built the app with these features:
- Video playback using YouTube links
- Audio playback through SoundCloud integration
- Toggle between video and audio modes
- Custom SoundCloud player with:
  - Play/pause controls
  - Volume adjustment
  - Progress bar
  - Playlist navigation
- Clean and intuitive user interface
- Responsive design for mobile and desktop

### 2. Deployment
I made the app accessible by:
- Hosting the code on GitHub
- Deploying the live version using GitHub Pages and OnRender.com
- Ensuring browser-based access for all users
- Testing cross-platform compatibility

## Special Thanks

This project wouldn't have been possible without:
- Claude.ai - For AI assistance and guidance
- GitHub - For reliable code hosting
- OnRender.com - For seamless web deployment
- SoundCloud - For audio streaming capabilities and API access
- YouTube - For video content integration
