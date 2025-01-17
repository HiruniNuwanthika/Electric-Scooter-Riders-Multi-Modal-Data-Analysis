# 🛴 Watch Out! E-scooter Coming Through!: Multimodal Sensing of Mixed Traffic Use and Conflicts Through Riders’ Ego-centric Views

| <a href="https://arxiv.org/" target="_blank">📃 Paper </a> |

## 🔥 Introduction

This repository contains gaze and speed data collected from e-scooter riders who followed a route comprising a pedestrian-shared path, a dedicated cycle lane, and a roadway.
* Gaze Data: Collected using Tobii Pro 3 Glasses
* Speed Data: Recorded continuously with a Garmin Edge 130 Plus bike computer

Additionally, we provide a sheet detailing the start and end timestamps for each route segment for every rider. 

## 📑 Table of Contents
- [🌟 Abstract](#-abstract)
- [📂 Repository Contents](#-repository-contents)
- [🛠️ Workflow](#-workflow)
  - [Gaze Data Analysis](#-gaze-data-analysis)
  - [Speed Data Analysis](#-speed-data-analysis)
  - [Fixation on Video ](#fixation-on-video)
- [📚 Citation](#-citation)

## 🌟 Abstract
E-scooters are becoming a popular means of urban transportation. However, this increased popularity brings challenges, such as road accidents and conflicts when sharing space with traditional transport modes. An in-depth understanding of e-scooter rider behaviour is crucial for ensuring rider safety, guiding infrastructure planning, and enforcing traffic rules. In this paper, we investigated the riding behaviours of e-scooter users through a naturalistic study. We recruited 23 participants, equipped with a bike computer, eye-tracking glasses and cameras, who traversed a pre-determined route, enabling the collection of multi-modal data. We analysed and compared gaze movements, continuous speed, and video feeds across three different transport infrastructure types: a pedestrian-shared path, a cycle lane and a roadway. Our findings reveal that e-scooter riders face unique challenges, including difficulty keeping up with faster-moving cyclists and motor vehicles due to the capped speed limit on shared e-scooters, issues in safely signalling turns due to the risks of losing control when using hand signals, and limited acceptance from other road users in mixed-use spaces. Additionally, we observed that the cycle lane has the highest average speed, the least frequency of speed change points, and the least head movements, supporting the suitability of dedicated cycle lanes -- separated from motor vehicles and pedestrians -- for e-scooters. These findings are facilitated through multimodal sensing and analysing the e-scooter riders' ego-centric view, which show the efficacy of our method in discovering the behavioural dynamics of the riders in the wild. Our study highlights the critical need to align infrastructure with user behaviour to improve safety and emphasises the importance of targeted safety measures and regulations, especially when e-scooter riders share spaces with pedestrians or motor vehicles.

## 📂 Repository Contents

- **Dataset**: .xlsx worksheets containing gaze data, .csv files with speed per second, and start and end timestamps for each route segment.
- **Source code**: Python scripts for pre processing and feature calculation.
- **Documentation**: Detailed documentation to help you get started with using the dataset.

## 🛠️ Workflow

<img src="./Figures/workflow.png" alt="workflow" style="width: 80%; height: auto;">

#### 👓 1 - Gaze Data Analysis
1. Segment gaze data into 3 route segments using the timestamps given in TimeMapping_BikeComputer_EyeTracker.xlsx sheet.
2. Extract fixation data
3. Select unique records
- Calculate gaze dispersion using average_acc_dispersion.py
- Calculate fixation count and fixation duration using average_fixation_count __fixation_duration.py 
- Calculate gaze dispersion using average_gaze_dispersion.py


#### ⏲️ 2 -Speed Data Analysis
1. Process speed data using speed_data_processing.py
- It includes timezone mapping
- segmentation (use TimeMapping_BikeComputer_EyeTracker.xlsx sheet)
- speed change point detection
- plotting
- mapping timestamp with video file.

#### 📹 3 -Fixation on Video 
Note: We have not included the recorded videos due to privacy concerns.
1. Extract fixation timestamps with x and y values of fixation point for each participant
2. Download fixation frames from the video

## 📚  Citation
If you use this data or code in your research, please cite our paper:

Thank you!
