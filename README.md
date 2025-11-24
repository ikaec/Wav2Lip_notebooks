# Wav2Lip_notebooks
Code and resources for multilingual lip-sync video generation.
## Steps to Generate a Video
  1. Download the required video
  2. Extract audio
  3. Transcribe audion to text and translate the text to a destination language.
  4. Create and audio using the translated text and clon the voice from the original video
  5. Standadize the audio and video and upload to google drive
  6. Upload the links of the files fron google drive
  7. Use the new audio and original video to perform lipsync

  ##  A -  Using the api_key:
  - This was successful with unpaid and later with paid plan. The paid plan then rejected further video generation. I then generated a new key which worked and you can see the output in the shared colab.
      - The demo is as in the notebook: French_to_English_LipSync_Uncrooped.ipynb, the notebook was run on colab.
      - Link to the tested video:  https://www.youtube.com/watch?v=32NNOzC_BAA&ab_channel=BFHTechnikundInformatik
      - The generated video output is in  _results_ .
      - Link to the generated file: https://private-sync-user-generations-v2.s3.amazonaws.com/generations/a8a9070b-ebdc-4788-a12f-dd32517d92c1/1f5122bb-dc1b-4ce1-a4c0-1fa1c0c3914c/french_to_en_lipsynced.mp4

  ##  B - Clonining a Wav2Lip git
  - clone https://github.com/Rudrabha/Wav2Lip.git
  - This approach has been described but has not worked with this video example.
  - The error has always been lack of face in some fraame.
    ##  B.1 - By trimming out slides without the face
            - I was able to work with a smaller video (trimmed from the original)
            - This led to an output result video
            - But the output is not as clear as the ones generated with the (key version)
    ##  B.2 - Using the full video, all processes remain the same but Wav2lip crashes with the errors shown:
    - raise ValueError('Face not detected! Ensure the video contains a face in all the frames.')
    - ValueError: Face not detected! Ensure the video contains a face in all the frames.

 ##  C - The results directory 
 - Contains generated lipsynced videos
    - The one using example from the repository looks good because the face covers most of the frame at all times and no empty frames. It is also shoter.
    - The one with our prepared data: Has a longer audio so the audio continues. It also has audio in regions where the frames have no face yet the original, these frames had a sound with a slide show.
    - I added the trimmed video`s out put files which include: The extracted face video, the cloned audio and the resulting output video in English
 ##  D - The Inputs directory 
 - There are files that are used as input in the different notebooks
   - The cloned verion uses the trimmed video
   - The other approach with the api_key uses was tested with te cropped video and uncropped and both had good output results   
