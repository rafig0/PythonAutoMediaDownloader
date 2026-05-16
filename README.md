# Python Automated Media Downloader

> A powerful and robust video downloader which can Download videos from virtually **any website** really fast.
> Powered by [`yt-dlp`](https://github.com/yt-dlp/yt-dlp) + **NetworkSniffer**.

---

## 🚀 What It Does

This Python script lets you download videos in **the highest available quality** from:
- **YouTube**
- **Vimeo**, **Dailymotion**, etc.
- And pretty much **any other website**

It’s lightweight, terminal-based, and crazy easy to use.

---

## 🏆 Highlights

✅ Download from YouTube and all supported sites directly  
✅ Save videos with their original title  
✅ Super clean CLI — no fluff  
✅ Works on Windows, Mac, and Linux  
✅ Download from *almost* any website using **NetworkSniffer + M3U8 link**  
✅ Insanely fast download speeds

---

## 🔍 How to Download from Any Website

Okay, here’s the secret sauce:

1. **Install [NetworkSniffer Extension](https://chromewebstore.google.com/detail/network-sniffer/fakcbdabfjjicnmkhljhanahlhdkjlgf)** (Chrome)
2. Go to the website and start playing the video.
3. Open the extension and look for a link that ends in `.m3u8`.
4. Copy that `.m3u8` link.
5. Paste it into this downloader when prompted.

⚠️ **WARNING Please be mindful**:  
This tool is meant for **educational and personal use only**.  
Always respect content creators, platforms’ terms of service, and copyright laws.  
If it’s not your content or you don’t have permission — don’t download it. 

---
## Code
```python
import yt_dlp #imports the yt_dlp library

def download_video(url):   #defines a function named download_video that takes one parameter url
    ydl_opts = {   #defines a dictionary named ydl_opts
        'format': 'best',  #downloads the best available quality
        'outtmpl': '%(title)s.%(ext)s',  #(output template) save the video with its title
    }
    with yt_dlp.YoutubeDL(ydl_opts) as ydl:  #with statement ensures that the resources are managed properly
        ydl.download([url])

if __name__ == "__main__":   #checks if the script is being executed as the main program
    video_url = input("Enter the video URL to be downloaded: ")   #asks the user for video link  
    download_video(video_url)
```

## 🛠 Requirements

- Python 3.6+
- [`yt-dlp`](https://pypi.org/project/yt-dlp/)

```bash
pip install yt-dlp
```

