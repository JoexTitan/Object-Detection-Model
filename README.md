
![Logo](https://blog-c7ff.kxcdn.com/blog/wp-content/uploads/2018/08/shutterstock_668209624-1.jpg)


# Object-Detection-AI-Model

The following AI model aims to identify objects in the video and predict the trajecory that they are moving in. The image processing algorithm will detect instances of semantic objects of a certain class (such as humans, buildings, or cars) in digital images and videos.

## Model Performance on Highway Traffic

<p>
  <img alight='center' alt='gif' src='https://github.com/JoexTitan/Object-Detection-AI-Model/blob/main/yolor/highway_traffic.gif?raw=true' width='850' height='500'/></p>


## Model Performance on Figure Skaters

<p>
  <img alight='center' alt='gif' src='https://github.com/JoexTitan/Object-Detection-AI-Model/blob/main/yolor/skating_detection.gif?raw=true' width='850' height='500'/></p>


## Model Performance on Mall CCTV Camera

<p>
  <img alight='center' alt='gif' src='https://github.com/JoexTitan/Object-Detection-AI-Model/blob/main/yolor/mall_detection.gif?raw=true' width='850' height='500'/></p>


## Model Performance on Soccer Players

<p>
  <img alight='center' alt='gif' src='https://github.com/JoexTitan/Object-Detection-AI-Model/blob/main/yolor/soccer_detection.gif?raw=true' width='600' height='800'/></p>



## Model Performance on a Tennis Player

<p>
  <img alight='center' alt='gif' src='https://github.com/JoexTitan/Object-Detection-AI-Model/blob/main/yolor/tennis_detection.gif?raw=true' width='600' height='800'/></p>


## Deploying your AI Model


Ensure that you have the following for both GPU and CPU Installations: 

- PyCharm Community Edition or any other IDE of your choice
- Anaconda (https://www.anaconda.com/products/distribution)
- NVIDIA Drivers (https://www.nvidia.com/Download/index.aspx)
- CUDA Toolkit (https://developer.nvidia.com/cuda-downloads)


GPU Installation, set-up a virtual environment with the following command

```bash
  conda env create -f environment.yml
```
Then activate your environment

```bash
  conda activate <Name_of_the_Project>
```

Check your compiler driver using

```bash
  nvcc --version
```


You should see the following

```bash
  nvcc: NVIDIA (R) Cuda compiler driver
  Copyright (c) 2005-2019 NVIDIA Corporation
  Built on Fri_Feb__8_19:08:26_Pacific_Standard_Time_2019
  Cuda compilation tools, release 10.1, V10.1.105
```

Make sure conda is saved in your Environment Variables

```bash
   C:\Users\Daniil_Zhilyayev\Anaconda3\Scripts

   C:\Users\Daniil_Zhilyayev\Anaconda3

   C:\Users\Daniil_Zhilyayev\Anaconda3\Library\bin
```

You are all set, here is a few commands for you to get started:

```bash
  python detect_track_trajectory.py --source videos/<File_Name01>.mp4 --cfg cfg/yolor_p6.cfg --weights yolor_p6.pt --conf 0.25 --img-size 1280 --device 0 --view-img

  python detect_track_trajectory.py --source videos/<File_Name02>.mp4 --cfg cfg/yolor_p6.cfg --weights yolor_p6.pt --conf 0.50 --img-size 1280 --device 0 --view-img

  python detect_track_trajectory.py --source videos/<File_Name03>.mp4 --cfg cfg/yolor_p6.cfg --weights yolor_p6.pt --conf 0.75 --img-size 1280 --device 0 --view-img
```

