# facial_emotion_recognition__EMOJIFIER
Recognizes the facial emotion and overlays emoji, equivalent to the emotion, on the persons face.  


## Making it work for you:  

There are 4 steps :


- **STEP 1** - generating the facial images 
   1. `cd </to/repo/root/dir>`  
   1. run `python3 src/face_capture.py --emotion_name <emotion-name> --number_of_images <number>`   
   -- example: `python3 src/face_capture.py --emotion_name smile --number_of_images 200`
   > This will open the cam and all you need to do is give the **smile** emotion from your face.
   - **NOTE: You must change /emotion_map.json if you want another set emotions than what is already defined.**
   - Do this step for all the different emotions in different lighting conditions.
   - For the above result, I used 300 images for each emotions captured in 3 different light condition (100  each).
   - You can see your images inside the **'images'** folder which will contain different folder for different emotion images.
    
- **STEP 2** - creating the dataset out of it  
   1. run `python3 src/dataset_creator.py`
   - This will **create the ready-to-use dataset** as a python pickled file and will save it in the dataset folder.
    
- **STEP 3** - training the model on the dataset and saving it  
    1. run `python3 src/trainer.py`
    - This will start the model-training and upon the training it will save the tensorflow model in the 'model-checkpoints' folder.  
    - It has the parameters that worked well for me, feel free to change it and explore.  
    
- **STEP 4** - using the trained model to make prediction  
    1. run `python3 src/predictor.py`
    - this will open the cam, and start taking the video feed -- NOW YOU HAVE DONE IT ALL. :clap:  
    
Its time to show your emotions :heart:

