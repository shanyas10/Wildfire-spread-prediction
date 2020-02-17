# Wildfire-spread-prediction
This project is aimed at demonstrating the importance of temporal features along with geographical features to detect wildfire spread using Spatio-Temporal LSTMs trained on GIS data along with GeoMAC’s dataset of wildfire perimeters. 

## Idea

Using spatio-temporal networks along with Earth science data from remote sensing, and Geographic Information System (GIS) as a prior to predict
near-future wildfire spread based on historical fire data.

## Problem Formulation
To formulate the problem mathematically, given a climate video X of length T with the each frame X<sub>i</sub> representing a 2D image with pixels representing burned areas 
(y<sub>i</sub><sup>(j,k)</sup> $ \epsilon $ {0,1}) along with geographical and atmospheric data for i ranging from 0 to T-1, the goal is to predict the areas surrounding the current fire that are expected
to burn (change in the value of pixels y<sup>j,k</sup> i ) in the subsequent n frames for i = T, ... T+n-1.
The ground truth y<sub>i</sub> is a 2-D matrix for i<sup>th</sup> time interval with each cell y<sub>i</sub><sup>j,k</sup>, i representing a pixel at jth row and kth column with value {1,0} representing burn.
