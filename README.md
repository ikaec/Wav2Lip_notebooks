# Wav2Lip_notebooks
Code and resources for multilingual lip-sync video generation.
## Steps to Generate a Video
  1. Download the required video
  2. Extract audio
  3. Transcribe audion to text and translate the text to a destination language.
  4. Create and audio using the translated text and clon the voice from the original video
  5. Standadize the audio and video and upload to google drive
  6. Upload the links of the files fron google drive
  7. Use the new audio and original video to perform lipsyn

  ##  A -  Using the api_key:
  - This was successful with unpaid and later with paid plan. The paid plan then rejected further video generation.
      - The demo is as in the notebook: French_to_English_LipSync_Uncrooped.ipynb, the notebook was run on colab.
      - Link to the tested video:  https://www.youtube.com/watch?v=32NNOzC_BAA&ab_channel=BFHTechnikundInformatik
      - The generated video output could not be uploaded here since it was too big.
      - Link to the generated file: https://private-sync-user-generations-v2.s3.amazonaws.com/generations/a8a9070b-ebdc-4788-a12f-dd32517d92c1/1f5122bb-dc1b-4ce1-a4c0-1fa1c0c3914c/french_to_en_lipsynced.mp4

  ##  B - Clonining a Wav2Lip git
  - clone https://github.com/Rudrabha/Wav2Lip.git
  - This approach has been described but has not worked with this video example.
  - The error has always been lack of face in some fraame.
