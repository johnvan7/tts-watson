# IBM Watson TTS

This package leverages IBM Watson's TTS A.P.I to stream audio of text using pyaudio. This uses apikey instead of username and password.

## Requirements

- **Python 2.7 or higher**
- **pip**
- **portaudio**[1]

[1] Can be installed with `brew install portaudio` (MAC OS) or `apt-get install portaudio19-dev` (Linux).

## CLI

Your Waston credentials will be initially requested. A config file located at `~/.config-tts-watson.yml` will be created. 

Run in the command line: `tts-watson text to sound i want`. You will hear `text to sound i want` played back to you.

## Example Of Usage

```python
from tts_watson.TtsWatson import TtsWatson

ttsWatson = TtsWatson('watson_apikey', 'en-US_AllisonVoice') #[2] 
ttsWatson.play("The text which i want to be a sound")
```

[2] `en-US_AllisonVoice` is one of many possible voices to use. You can see the full list [here](https://www.ibm.com/watson/developercloud/text-to-speech/api/v1/#get_voice) and descriptions [here](https://www.ibm.com/watson/developercloud/text-to-speech/api/v1/#get_voices).

