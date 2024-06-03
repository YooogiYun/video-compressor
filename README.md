## Video Compressor

### About

- A script that uses ffmpeg to compress videos for free
- It uses Python as a terminal interface for inputting options

### Prerequisites

- Make sure to install the followings:

    **Linux:**
  - `sudo apt install ffmpeg`
  - `sudo apt install python3`
  - `sudo apt install sox`
    <br>

    **Windows:**
  - Download [ffmpeg here](https://www.ffmpeg.org/)
  - Set ffmpeg to `$PATH` or place ffmpeg.exe in the `same directory of executable file`

### Instruction

![VideoCompressor](https://github.com/YuniqueUnic/video-compressor/assets/127641096/4f4c59dc-a974-4c0a-8eec-0265aad14d78)

**For Multiple File Compression:**

- Create a directory for the uncompressed files
- _Be inside of this directory and_ run `python3 main.py` or run `make` in terminal
- Answer the prompt amd wait for the files to finished _(For default settings just hit `ENTER`)_
- Once finished, the compressed files are found in the `compressed` folder in the original file(s) folder

**Sample Prompts**

Sample 1. Single File

```powershell
   [INFO] Successfully found FFMPEG in application directory.
          --> FFMPEG path: C:\Users\Administrator\Desktop\video-compressor\ffmpeg.exe
   [INFO] If it is a folder, compress all videos in that folder.
   [INFO] If it is a single video file, compress that file directly
   [PROCESS] Target Path:
   > "F:\ScreenRecordings\Video1.mp4"
   1. F:\ScreenRecordings\Video1.mp4
       -> F:\ScreenRecordings\compressed\Video1.mp4
   
   [PROCESS] Compression Rate [0-51] (Default: 26):
   > 25
   [PROCESS] Frames Per Second (Default: 25):
   > 30
   [PROCESS] Video Codec (None/H264/H265/MPEG4) [0-3] (Default: 0):
   > 0
    ------------START COMPRESSION---------------
```

Sample 2. Folder with videos

```powershell
   [INFO] Successfully found FFMPEG in SYSTEM PATH.
   [INFO] If it is a folder, compress all videos in that folder.
   [INFO] If it is a single video file, compress that file directly
   [PROCESS] Target Path:
   > "F:\ScreenRecordings"
   1. F:\ScreenRecordings\Video1.mp4
       -> F:\ScreenRecordings\compressed\Video1.mp4
   2. F:\ScreenRecordings\Video2.mp4
       -> F:\ScreenRecordings\compressed\Video2.mp4

   [PROCESS] Compression Rate [0-51] (Default: 26):
   > 25
   [PROCESS] Frames Per Second (Default: 25):
   > 30
   [PROCESS] Video Codec (None/H264/H265/MPEG4) [0-3] (Default: 0):
   > 0
    ------------START COMPRESSION---------------
```

- where compression rate is the rate of compression to be processed,
  means it will have a higher compression but will have worse quality.

- the output folder automatically generated and is found on
  the sub newly created compressed folder: such as F:\ScreenRecordings\compressed\

### Features

- [x] Support SYSTEM PATH FFMPEG / Root directory FFMPEG
- [x] Support dragging files/folders or them together into executable file to process them
  - [x] Automatically filter the file(s) with video type
  - [x] Support single video compression
  - [x] Support Mutiple videos compression
- [x] Support custom the params for FFMPEG to compress the video(s)

### Notes

- Make sure to have a faster cpu to increase faster compression time
- Tested on a Quad Core CPU where each process can take from 4-5min depending on the footage size and the file size.

 Best to be run on a Quad Core CPUs and above since on Dual Core CPUs it runs slow af running at 30min per compression...
