---
title: "Creating Narration Audio"
date: 2024-05-12 15:00:00 +0900
tags:
- "NaturalReader"
- "OBS Studio"
- "FFmpeg"
- "Audacity"
categories:
- "Speech"
slug: create-narration-audio
draft: false
---

In the previous post, I discussed how to create a speech draft.  
Now, I'll explain how to create a narration audio file based on the prepared speech script.

## Using Software

I use the following software:

| Software | Description |
| --- | --- |
| [NaturalReader online](https://www.naturalreaders.com/) | It reads the text aloud in a natural voice. |
| [OBS Studio](https://obsproject.com/) | It records the desktop screen, including audio. |
| [FFmpeg](https://ffmpeg.org/) | It extracts MP3 audio from video files. |
| [Audacity](https://www.audacityteam.org/) | It's a digital audio editing software. |

{{<alert title="Note" color="primary">}}
Detailed setup and operation instructions for each software are omitted here.
{{</alert>}}

### Natural Reader online

![NaturalReader screenshot](/studylog/imgs/2024-05-12-natural-reader.png)

NaturalReader online offers enough free reading for speeches lasting up to one minute.   
In practice, this free range extends to approximately 20,000 characters.  
Also, since downloading audio files directly from NaturalReader is a paid feature, I always use an alternate method to extract the audio files.

### OBS (Open Broadcast Software) Studio

![OBS Studio screenshot](/studylog/imgs/2024-05-12-obs-studio.png)

While NaturalReader reads the text, I use OBS Studio to capture the desktop screen, saving it as an MP4 video file.   
The image above shows my script being read by NaturalReader online, with the screen captured using OBS Studio.

### FFmpeg

After that, I use FFmpeg to extract an MP3 audio file from the MP4 video.  
Here's the command prompt for extracting the MP3:

```
❯ ffmpeg -i narration.mp4 -vn narration.mp3
```

### Audacity

![Audacity screenshot](/studylog/imgs/2024-05-12-audacity-screenshot.png)

When recording screen captures with OBS Studio, it's common to end up with silent sections at the beginning and end of the recording.   
To address this, I use Audacity, an audio editing software, to trim out the unnecessary silent parts (<span style="color: red; ">highlighted in red in the diagram</span>) and extract the narration audio file.  
The image above shows my script's narration audio being edited in Audacity.

The following is a sample audio narration of [the script for Exercise 1 from Engoo's Photo Desctiption Lesson 1](/studylog/docs/engoo_photos/intermediate/lesson01/#exercise-1-at-the-doctors-office).
<figure>
  <audio controls src="/studylog/audios/2024-05-12-narration.mp3">
</figure>

This is how I create a narration audio file that closely resembles natural speech from the speech manuscript.
