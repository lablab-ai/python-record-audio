# Python record audio
How to record microphone audio with pyhton - Code Snippet

```python
import sounddevice as sd
from scipy.io.wavfile import write

def record(duration):
    fs = 44100  # this is the frequency sampling; also: 4999, 64000
    myrecording = sd.rec(int(duration * fs), samplerate=fs, channels=2)
    print("Starting: Speak now!")
    sd.wait()  # Wait until recording is finished
    print("recording finished")
    write('output.mp3', fs, myrecording)  # Save as MP3 file
    
 record(10) # 10 seconds
```
This will create a new `.mp3` file in your current working directory

---

[![Artificial Intelligence Hackathons, tutorials and Boilerplates](https://storage.googleapis.com/lablab-static-eu/images/github/lablab-banner.jpg)](https://lablab.ai)


## Join the LabLab Discord


![Discord Banner 1](https://discordapp.com/api/guilds/877056448956346408/widget.png?style=banner1)  
On lablab discord, we discuss this repo and many other topics related to artificial intelligence! Checkout upcoming [Artificial Intelligence Hackathons](https://lablab.ai) Event


[![Acclerating innovation through acceleration](https://storage.googleapis.com/lablab-static-eu/images/github/nn-group-loggos.jpg)](https://newnative.ai)
