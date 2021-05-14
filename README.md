# Voice-Conversion
We have implemented a Transformer based Text-to-Speech model in the python notebook which takes text as the input and output the mel spectogram generated by the model.
We would suggest to run the notebook on google colab.
The basic pipeline for the whole system is:
1. Audio as input:- convert it into text using ASR models
2. Pass the text into the TTS model to get mel spectograms
3. Use the mel spectogram to generate audio file

The generated mel spectograms were then used by the espnet recipe to generate the audio files using different vocoders(Griffin-Lim, parallel-wavegan and wavenet).
Please refer to the git repository of espnet https://github.com/espnet/espnet and go to egs/vcc20/vc1_task1/ folder to understand the recipe to generate the audio files.
Since espnet provides a similar TTS transformer model, we have used the espnet functions to get inferences, generating graphs and log files.
