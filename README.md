Audio profanity is a big headache and while it seems small but if you're working with age sensitive research or projects. You would want to rate your audio and know more about it. that's where this simple project come into play. it uses OpenAI whisper model to segment audio and let you know before it becomes a headache. 

### What can be done?
Honestly, tons! For starters I have written a simple substring based matching algorithm that can match and compare from a list of curse words released by CMU (Carnegie Mellon). Find more info: https://www.cs.cmu.edu/~biglou/resources/bad-words.txt 

1. Segment the audio and extract the transcriptions (not intended rather a byproduct)
2. Extract wordlist of your audio
3. and then do matching

I have more ideas in mind and gonna maintain this like a dedicated religion. Because I have a newfound interest in audio segmentation. 

### How it works?

Good question! 

```Python
from audiocencesored import *

# this func transcribes your audio. I didn't harcode file-name
transcribe_timestamps(audio_file, output_file)

# extracting the words from transcript
extract_words(json_file, output_file)

# let's download the CMU list
download_list(output_file="bad_words.txt")

# checking the score
check_profanity(word_list_file, bad_words_file, rating="R")
```

### Anything to keep in mind?
Certainly! Have your audio files in `.wav` format. 

Disclaimer: It's meant to be fun-project while providing support and feature is suppose to be religion for me. Drop a hi, on github if you have some features in mind. https://github.com/sleepingcat4/audio-profanity https://colab.research.google.com/drive/1myh2W3f4HMXGnAdfb0OanC3f8QhyBKIZ?usp=sharing
