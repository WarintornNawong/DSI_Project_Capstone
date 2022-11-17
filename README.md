## Project Titlte : Oil Spill Detection From Satellite Imagery.

## ✈️Problem Statement

To develop OIL Spill Detection from Satellite Images in order to build spilling detection system for related government agency i.e. Department of Coastal Resource, Ministry of Natural Resources and Environment.

![image](https://user-images.githubusercontent.com/104628789/202325738-b8dea3f4-9d30-4d21-ba03-60a442815364.png)


**1. Reactive Detection**

To identify oil spilled properties i.e. Location, Size of Spilled Boundary etc. to launch the oil spill response plan according to IMO/UNEP Standard and Guidelines.
    
    
    
**2. Proactive Detection**

To establish the schedule-based ocean monitoring to ensure the compliance of oil spill prevention of related operator. 
    
## 🚀 Background

An oil spill is the release of a liquid petroleum hydrocarbon into the environment, especially the marine ecosystem, due to human activity, and is a form of pollution. The term is usually given to marine oil spills, where oil is released into the ocean or coastal waters, but spills may also occur on land. Oil spills may be due to releases of crude oil from tankers, offshore platforms, drilling rigs and wells, as well as spills of refined petroleum products (such as gasoline, diesel) and their by-products, heavier fuels used by large ships such as bunker fuel, or the spill of any oily refuse or waste oil. (Wikipedia)
    
    
### The consequence of Oil Spill
 
![image](https://user-images.githubusercontent.com/104628789/202326226-e24537e5-e6be-45bf-b26b-115ba99f0e5d.png)




**1. Environmental Impacts**

Major oil spills are bad for the environment because they damage wildlife, marine ecosystems, and coastal environments. spilled oil can affect animals and plants in two ways: dirесt from the oil and from the response or cleanup process. oil spills can also harm air quality. The chemicals in crude oil are mostly hydrocarbons that contains toxic chemicals such as benzenes, toluene, poly-aromatic hydrocarbon and oxygenated polycyclic aromatic hydrocarbons. These chemicals can introduce adverse health effects when being inhaled into human body. (Wikipedia)
    
**2. Economical Impacts**

Oil spills can lead to severe disruption for the tourist industry. Contamination of coastal areas with high amenity value is a common feature of many oil spills. In addition to costs incurred by clean-up activities, serious economic losses can be experienced by industries and individuals dependent on coastal resources.(ITOPF)


**3. Human Impacts**

An oil spill represents an immediate negative effects on human health, including respiratory and reproductive problems as well as liver, and immune system damage. Oil spills causing future oil supply to decline also effects the everyday life of humans such as the potential closure of beaches, parks, fisheries and fire hazards. (Wikipedia)
    
    
### The cause of Oil Spill

Oil Spill can caused from main source with the following items, 

1. Oil Tanker/Transport Vessels

2. Oil Rig/Platform

3. Pipeline

4. Storage Tank


## 💂🏼‍♂️ Dataset ##

The dataset is derived from the Roboflow websites which include the SAR (Synthetic Aperture Radar) Oil spill with the original data from 1000 datasets which is split into train, val, test for 700,200 and 100 respectively. However, The data provider has prelimiary augmented train set to increase number of train dataset with the following condition,

-    Crop : 0 - 37 %.
-    Rotation : -5 to 5.
-    Brightness : -30 - 0.
-    Blur : Up to 2 Px.
-    Noise : Up to 10 % of pixel.

**Dataset Name** : SARImgV3

**Data Provider** : Matteo Attimonelli

**Data Type** : Synthetic Aperture Radar (SAR).

URL Link : 'https://universe.roboflow.com/matteo-attimonelli1999-gmail-com/sarimgv3'

## Example of Train Set

![image](https://user-images.githubusercontent.com/104628789/202325986-e1e4f226-04a6-42c1-a40e-04357e317727.png)

## REAL CASE TEST DETECTION

To test the real oil spill events around by selecting the difference location around the world i.e. USA, Peru, Spain etc. and difference type of satellite mission i.e. Sentinel 1/2, ERS-1/2 etc.

![image](https://user-images.githubusercontent.com/104628789/202326157-2d78d180-90b8-492e-a657-5e79e28ae0cb.png)

## MODEL YOLOV7

#### What is YOLOv7?
The YOLO (You Only Look Once) v7 model is the latest in the family of YOLO models. YOLO models are single stage object detectors. In a YOLO model, image frames are featurized through a backbone. These features are combined and mixed in the neck, and then they are passed along to the head of the network YOLO predicts the locations and classes of objects around which bounding boxes should be drawn.

![image](https://user-images.githubusercontent.com/104628789/202326415-0d74cb4a-d74e-4c24-bc11-b9da90cd351a.png)

The evaluation of YOLOv7 models show that they infer faster (x-axis) and with greater accuracy (y-axis) than comparable realtime object detection models.

The github link the YOLOV Version 7 is 'https://github.com/WongKinYiu/yolov7' 

#### The example file of YOLO Detection

![image](https://user-images.githubusercontent.com/104628789/202326499-26b52b4b-e241-4f17-a6df-59494b9ec298.png)

## MODEL CASE.

The model Case for runnning to maximize the performance and reliability of the object detection model.

1. FIRST CASE - 200 EPOCHS
2. SECOND CASE - 300 EPOCHS
3. THIRD CASE - ADD AUGMENTED NON-LINE SHAPE FOR 300 PICTURES
4. FORTH CASE - ADD AUGMENTED NON-LINE SHAPE FOR 900 PICTURES.
5. FIFTH CASE - ADD 90 ROTATION OF CASE 3.
6. SIXTH CASE - ADD 90 ROTATION OF NEW AUGMENTATION METHOD.


## BASELINE RESULTS
The error analysis in baseline showed there are two issue about the model prediction.

![image](https://user-images.githubusercontent.com/104628789/202327515-2b7fb365-6632-4d10-a610-67e57023629e.png)
 

## POST-AUGMENTATION RESULTS

the Results of real case detection from 'Oil Spill Case from Caspian Sea, Azerbaijan' and 'Oil Spill Case from Latakia, Syria to Cyprus' which showed that they could detect the non-line spill shape after doing the augmentation at least 300 pictures.

![image](https://user-images.githubusercontent.com/104628789/202326880-6a919d2c-7822-4f84-b405-35a290f4916f.png)


## BEST MODEL PREDICTION

![image](https://user-images.githubusercontent.com/104628789/202326915-22d4da3c-4feb-4190-889d-15f0ca816011.png)


## MODEL COMPARISON

The table below showed the comparison between test metrics of post-augmented model which **CASE-5** ( non-line shape augmentation with applying additional 90 degree rotation) provided the best score in Recall , Max F1 Score, mPA@ IoU > 0.5, mPA@ IoU > 0.5 and < 0.95.

![image](https://user-images.githubusercontent.com/104628789/202327014-0fd4ca06-e605-4ebc-a508-168ee7782662.png)

## Model Constraints

![image](https://user-images.githubusercontent.com/104628789/202327376-4698950e-a947-4385-8cf6-41ca240753c1.png)


## CONCLUSION

The reason above I decided to apply the CASE-5 Model to use for developing "Oil Spill Detection System".

![image](https://user-images.githubusercontent.com/104628789/202327345-7e3dcedb-d896-4383-9d01-b64d5743f451.png)





