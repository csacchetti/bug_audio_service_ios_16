# bug_audio_service_ios_16




## This project shows the audio_service bug that started to occur after the update to iOS 16

Description of the bug - When using the play command after loading a new audio file when the app is in the background the audio frezzes

### Reproduction steps

First of all, download the example from GitHub.
The code is that of the main of the example in audio_service gitHub.
I have only added the final part where I put the explanations to reproduce the bug and I added in the construct of AudioPlayerHandler() the function _myListenVoiceState();

To check this, go to the end of the song and go back 10 seconds by clicking
on the back button and then start play. If you are not in the background
the song once it reaches the end will resume normally, whereas if you start
play and go into the background the song if you are on iOS 14 will behave correctly
and restart, whereas if you are on iOS 16.2 it will freeze.
