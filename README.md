# Shoplifting-Detection-Through-Mediapipe-and-LSTM

## Instructions for setting up the environment:
1. Create a virtual environment using the following command in Anaconda
    conda create --name myenv pyhton==3.8.0
2. Install the required libraries from requirements.txt using the following command
    pip install -r requirements.txt
3. If you want to train the model: 
    Run train.ipynb file
    i. Change the paths of the dataset and where the model will be saved.
    ii. Run all the cells
    
    Make sure that the data matches the following criteia
    i. There can't be any header
    ii. Number of row in the Dataset must be a multiple of window_len variable. 
    iii. For every window_len number of data, there must be a class in the target csv file. 0 for normal, 1 for shoplifting was used during training.
4. To test the model:
    Run Framework.ipynb file
    i. Set the video path or camera id 
    ii. set the model path
    iii. run the cells
    Note: If you want to stay the color when shoplifter is detected, comment out 129,130 number line
5. To create dataset from video:
    Run Dataset_Maker.ipynb
    i. Change the path of the video
    ii. Set window_len as you needed
    iii. Change the order of data points if needed.
    iv. Set the second argument of csv open line to 'w' if this is the first time of running the code.
    v. Set the second argument to 'a' if you want to merge multiple videos together.
    vi. Run the cells
