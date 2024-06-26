# YouTube Top played downloader with GUI

## A YouTube / YouTube Music utility allowing you to download your most played songs

- analyzes your watch history, based on the json file you provide from Google Takeout
- you can choose the number of top songs to download

Perfect for trips without internet access, where you still want to bring your favourite music with you. Or just for creating a local backup of your beloved music 😌

## How to use:
Currently you you need a java IDE to run this
1. Download your Google Takeout data from https://takeout.google.com/ (scroll down to YouTube and select only the "watch history" option, don't forget to set the format to JSON. then follow the instructions to download the data)
2. Unzip the downloaded file and navigate to the "YouTube and YouTube Music" folder
3. Find the "watch-history.json" file and provide it to the application
4. Choose the number of top songs you want to download
5. Click the "Download all" button and wait for the download to finish

Works only for Windows, due to yt-dlp.exe executable file.

## Preview:
<img width="1000" src="https://raw.githubusercontent.com/MarosLodnipeguh/yt-top-played-download/master/preview.png" alt="" />

## Technologies used:
- Java with JavaFX (fxml + CSS) for the GUI
- Jackson library for parsing the json file
- [yt-dlp project](https://github.com/yt-dlp/yt-dlp) for downloading the audio files
- Java ProcessBuilder for running the yt-dlp.exe process

## TODO / Future improvements:
- [ ] Java executable for Windows
- [ ] Console logs pass to the GUI, non-blocking, currently the GUI freezes during the download process
- [ ] Add a progress bar for the download process
- [ ] Threaded downloading process
- [ ] Show artists in the list
- [ ] Lazy background image loading, with a blurry placeholder for the list view (non-blocking for the UI)
- [ ] Charts for the top artists, top genres, etc. (in a separate tab)
- [ ] Audio downloader with trimmer using ffmpeg (in a separate tab, basically a GUI for yt-dlp with trimming capabilities)
- [ ] Add a auto updater for yt-dlp.exe
