# TTS-Demo2

## Notes about TTS 
From [StackOverflow](https://stackoverflow.com/questions/40820177/what-is-the-difference-between-chrome-tts-google-tts-cloud-speech-api-and-and)

"Cloud Speech API" is the only one converting speech to text. All the others convert text to speech.

"Chrome TTS" is for the Chrome browser, "Android TTS" is the API to use text-to-speech in Android apps and "Google TTS" is a TTS engine which can be used via the "Android TTS" API


## Points moving forward
- Main Problem 
  - ** Android chrome does not have the default listed voices **
      WEB SPEECH API WILL NOT WORK
  - Current Speech has a long break during one of the question.... can we refactor the code to make it better? But it still does not sound human enough.
  (_Was able to figure out the long pause at the end of every question was due to a line break that I had on my code editor_)
  - Steps toward a solution
    - Use Android TTS, googleTTS, or use onmark boundaries (won't work)
    - will you be able to use a chrome extensions and add to it? (won't work)  
    - Use Android Studio? (Really might be best option) 

- Issues at hand are it is difficult to find code examples for TTS on chrome, not familiar with Java, and googleTTS is free up untill 4 million characters 

## Important Links 

### Chrome

- [Chrome source code only jsons](https://chromium.googlesource.com/chromium/chromium/+/3d79ca55eb86e0f8733585beaece851e961ac769/chrome/common/extensions/api/)
- [Using chrome TTS](https://stackoverflow.com/questions/25641521/using-chrome-text-to-speech-in-a-chrome-extension)
- [Youtube video explaining how to set it up](https://www.youtube.com/watch?v=5KL_ccQwAuo)
- [Chromium's readme about tts](https://chromium.googlesource.com/chromium/src.git/+/refs/heads/lkgr-ios-internal/docs/accessibility/tts.md#text-to-speech-in-chrome-and-chrome-os)

*Chrome uses the same Text to Speech Engine as Web Speech API*

### Android
- [Android's Text To Speech](https://developer.android.com/reference/android/speech/tts/package-summary)
- [Stack Overflow TTS Example with Java](https://stackoverflow.com/questions/3058919/text-to-speechtts-android)
- [Example Getting Started](https://android-developers.googleblog.com/2009/09/introduction-to-text-to-speech-in.html)

*This library just sends the message to browser Engine*

### Google Cloud TTS 
-[Introduction](https://cloud.google.com/text-to-speech)
- [Stack Overflow of using Google Cloud TTS](https://stackoverflow.com/questions/15653145/using-google-text-to-speech-in-javascript)

#### Really might be the best option (Just after 5 million character's are spoken it is not free)
---

Plan of actions: 
Create a manifest json file to inject the content/background script into assessment and write [permissions: tts] => Use chrome.tts.speak
OR
Use Android's Studio
OR 
Use googleTTS
