# Compatible Phones Research

# Introduction 
The goal of this report is to search for all compatible phones for HoloKit X in the market. 

We first listed all the necessary criteria that current HoloKit X design limits. 
Then we will search on the smartphone database [gsmarena.com](https://gsmarena.com) to find all compatible phones. Finally, we will do some smartphone market predictions for the future compatibility of HoloKit X in its life cycle. 

# Criteria 
The current HoloKit X was designed for iPhone 11 Pro. 


## Dimensions 

### Height 
* **[C1] Height:  > 135mm**
- The width of HoloKit X perfectly fits phones with 144mm height (iPhone 11 Pro)
- Phone with too small height may not cover full FOV. 
- Required.
* **:ok:[C2] Height: < 152mm**
- Phone with too much larger height makes it hard to symmetrically align the phones and HoloKit. 
- Each side has no more than 4mm extra is a good UX for alignment. 
* **:-1:[C2-] Height: < 170mm**
- Usable. But bad UX for alignment. 

### Thickness
* **[C3] Thickness: > 7mm** 
- The small thickness may not secure the phones in the holder. 
- Required.
* **[C4] Thickness: < 9mm**
- The too much larger thickness of phones will break the holder of HoloKit. iPhone 11 Pro has an 8.1mm thickness.
- Required.

### Weight 
* **:ok:[C5] Weight: < 200g**
- We don't want to put too much weight on the user's nose and head. Even 200g is hard to wear for more than 15 minutes. 
* **:-1:[C5-] Weight: < 230g**
- Less strict weight limitation. 

## Image Quality  
* **:ok:[C6] Display Density: > 420ppi**
- The viewing window size of HoloKit X per eye is 50mm (vertical). HoloKit X field of view (vertical) is 40 degrees. We want to achieve at least 20 PPD (pixel per degree). 
- 50mm / 25.4 (mm / inch) * 420 ppi / 40 = 20.66 ppd 
* **:-1:[C6-] Display Density: > 320ppi**
- Less Clear Imaging Quality. 
- 50mm / 25.4 (mm / inch) * 320 ppi / 40 = 15.7 ppd 
* **:ok:[C7] Display Technology: OLED**
- Black is transparent in mixed reality. LCD Screen can not display a completely dark black.  
* **:-1:[C7-] Display Technology: LCD**
- Usable. Less transparency.
* **:ok:[C8] Display Refresh Rate: >=60Hz**
- Standard refresh rate.
- Required.
* **:+1:[C8+] Display Refresh Rate: >=90Hz**
- Lower latency for the better user experience of hologram stability.

## Sensor 
* **[C9] With an ultrawide camera**
- Ultrawide camera (12mm equivalent focal length or around 120 diagonal FOV) makes hand tracking possible. 
* **[C10] Time-of-Flight (ToF) Camera**
- It's necessary for environmental understanding (mesh generation). 
- It's better for AR plane finding, and fast calibration.

## AI Engine
* **:+1:[C11+] AI Benchmark: DeeplabV3 100 FPS or above**
- Reasonable benchmark to achieve a 60FPS real-time hand tracking performance. 
- Hopefully, A14 can achieve this criterion.

* **:ok:[C11] AI Benchmark: DeeplabV3 50 FPS or above**
- Real-time hand-tracking requires strong neural network computing hardwares. 
- Only A13 or above / Snapdragon 865 or above can achieve this criterion. 
- Reference: Master Lu (AI Mark 3) [AI Benchmark](https://www.anandtech.com/show/15207/the-snapdragon-865-performance-preview-setting-the-stage-for-flagship-android-2020/4)
* **:-1:[C11-] No AI for Hand tracking**
- An external 3DOF or 6DOF controller is required for this criterion. 

# Results

## iOS 

### Comparisons 
| Phones | Height | Weight | Display | Hand Tracking <br> (Ultrawide + AI) | ToF | UX Tier | Remark |
| ------ | ------ | ------ | ------- | ------------------------------ | --- | ------- | ------ |
| iPhone 12 Pro :question: | :ok: | :ok:	| :+1: | :+1: | :+1: | Excellent <br> :star::star::star::star::star: |  |
| iPhone 12 :question: | :ok: | :ok:	| :ok: | :+1: |  | Nice <br> :star::star::star::star: |  |
| iPhone 11 Pro | :ok: | :ok: | :ok: | :ok: |  | Nice <br> :star::star::star::star: |  |
| iPhone 11 | :ok: | :ok: | :-1: | :ok: |  | Good <br> :star::star::star: |  |
| iPhone 12 Pro Max :question:  | :-1: | :-1: | :+1: | :+1: | :+1:| Nice but heavy <br> :star::star: |  |
| iPhone 11 Pro Max | :-1: | :-1: | :ok: | :ok: |  | Nice but heavy <br> :star::star: |  |
| iPhone XS | :ok: | :ok: | :ok: | :x: |  | Fair <br> :star:  | Controller required |
| iPhone X | :ok: | :ok: | :ok: | :x: |  | Poor  <br> :star: | Controller required |
| iPhone XS Max | :-1: | :-1: | :ok: | :x: |  | Fair and heavy <br> :star: | Controller required |
| iPhone XR | :ok: | :ok: | :-1: | :x: |  | Poor <br> :star: | Controller required |

Remark: 
:question: means rumored or predicted.

Note: 
* iPhone 12 Pro will have excellent UX for AR with all features. 
* iPhone X, XS, XS Max, XR will require a controller to operate. It's not so good for our product strategy, we don't want to make a 3DOF controller.

Rumors for iPhone 12 Pro:
* A14 (5nm) will be introduced and will double the power of AI engine for hand tracking.
* ToF Camera will be introduced. It's an essiential component of AR environmental understanding.
* 90Hz or 120Hz screen will be introduced. It will improve the latency which is essiential to AR. 
* OLED screen will be introduced to iPhone 12. 

So predictively iPhone 13 series will have all these features. It will make HoloKit X UX in excellent status. 

## Android 

| Phones | Height | Weight | Display | Hand Tracking <br> (Ultrawide + AI) | ToF | UX Tier | Remark |
| ------ | ------ | ------ | ------- | ------------------------------ | --- | ------- | ------ |
| Samsung Galaxy S20 / S20 5G | :ok: | :ok:	| :ok: | :ok: | | Nice <br> :star::star::star: |  |
| Samsung Galaxy S20+ / S20+ 5G | :-1: | :-1:	| :ok: | :ok: | | Nice but heavy <br> :star::star: |  |
| Samsung Galaxy S20 Ultra / S20 Ultra 5G | :-1: | :-1:	| :ok: | :ok: | :+1: | Nice but heavy <br> :star::star: |  |
| Sony Xperia 1 II | :-1: | :ok: | :ok: | :ok: | | Fair <br> :star: | | 
| Samsung Galaxy S30 :question: | :ok: | :ok: | :+1: | :+1: | :+1: | Excellent :star::star::star::star::star: | Snapdragon 875 (5nm) | 
| OnePlus 8 Pro :question: | :-1: | :ok: | :+1: | :ok: | | Nice but heavy <br> :star::star: | 
| Huawei P40 Pro :question: | :-1: | :-1: | :+1: | :ok: | :+1: | Nice but heavy <br> :star::star: | 

Remark: 
:question: means rumored or predicted.

# Conclusions

## Tier 1. 
Our product will primarily target for 
* iPhone 14 Pro
* iPhone 13 Pro
* iPhone 12 Pro

* iPhone 14 Pro Max
* iPhone 13 Pro Max
* iPhone 12 Pro Max

Lidar sensor-enabled.

NFC verification is preferred for these phones.

## Tier 2.
Enough CPU but no LIDAR 

* iPhone 14
* iPhone 13
* iPhone 12

## Tier 3.
Weak CPU but works

* iPhone X
* iPhone XS
* iPhone XS Max
* iPhone 11 Pro 
* iPhone 11 Pro Max
