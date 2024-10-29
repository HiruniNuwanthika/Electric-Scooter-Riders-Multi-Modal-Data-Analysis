**Gaze Data Analysis**
1. Segment gaze data into 3 route segments using the timestamps given in TimeMapping_BikeComputer_EyeTracker.xlsx sheet.
2. Extract fixation data
3. Select unique records
-Calculate gaze dispersion using average_acc_dispersion.py
-Calculate fixation count and fixation duration using average_fixation_count __fixation_duration.py 
-Calculate gaze dispersion using average_gaze_dispersion.py


**Speed Data Analysis**
1. Process speed data using speed_data_processing.py
-It includes timezone mapping, segmentation, speed change point detection, plotting and mapping timestamp with video file.


**Fixation on Video**
1. Extract fixation timestamps with x and y values of fixation point for each participant
2. Download fixation frames from the video

