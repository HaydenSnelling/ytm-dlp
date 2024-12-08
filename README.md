# ytm-dlp

`ytm-dlp` is a Bash script designed for downloading audio from YouTube Music / YouTube using `yt-dlp`. It simplifies the download process by abstracting away the need to remember various command-line flags, making it easier to use without a graphical user interface.

## Getting Started

To get started, ensure the script is in your PATH and run it without any arguments to see the following help page.
## Help page
```
Usage: ytm-dlp [OPTIONS] <URL|path_to_file>

Basic Usage:
  To download an MP3 file with cover art:
    ytm-dlp https://music.youtube.com/watch?v=yK-6yAt3c-U

  To download without cover art:
    ytm-dlp --no-art https://music.youtube.com/watch?v=yK-6yAt3c-U

Additional Cover Art Options:
  If you are downloading a song without official cover art like a mashup or fan made remix,
  The center of the thumbnail will be used as the cover art.

  If this is not to your liking you can use the following options to choose a different part of the thumbnail
to use as the cover art.

Cover Art Options:
  --art-left      Crop cover art to 1:1 ratio (left-aligned)
  --art-right     Crop cover art to 1:1 ratio (right-aligned)
  --art-mid-left  Crop cover art to 1:1 ratio (mid-left aligned)
  --art-mid-right Crop cover art to 1:1 ratio (mid-right aligned)

  --normal-art    Keep original cover art without cropping
  --no-art        Skip embedding of cover art entirely

  Example for adjusting cover art (useful for mashups or fan remixes):
    ytm-dlp --normal-art https://music.youtube.com/watch?v=yK-6yAt3c-U
    ytm-dlp --art-mid-left https://music.youtube.com/watch?v=yK-6yAt3c-U

Playlist and Album Download:
  You can use a URL of an album or any playlist to download all songs:
    ytm-dlp https://music.youtube.com/playlist?list=PLMC9KNkIncKtPzgY-5rmhvj7fax8fdxoj

Batch Download:
  To queue multiple album downloads, create a file with URLs on separate lines:
    https://music.youtube.com/playlist?list=PLMC9KNkIncKtPzgY-5rmhvj7fax8fdxoj
    https://music.youtube.com/playlist?list=OLAK5uy_nYdU5PuoUEB0l1waLasIRvqMC2PzWRjMg

  To automatically download each album into its own folder, add the folder name in quotes:
    https://music.youtube.com/playlist?list=PLMC9KNkIncKtPzgY-5rmhvj7fax8fdxoj "Best Hits"
    https://music.youtube.com/playlist?list=OLAK5uy_nYdU5PuoUEB0l1waLasIRvqMC2PzWRjMg "MM..FOOD"

Chapter Splitting:
  Use --split-chapters to save each chapter as an individual song:
    ytm-dlp --split-chapters https://music.youtube.com/watch?v=example

Other Options:
  --help          Display this help message

  --no-artist     Exclude artist name from the output filename
```
