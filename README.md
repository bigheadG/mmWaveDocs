# mmWaveDocs
mmWave Documents

## V01 Vital Signs Lab
## V02 High Accurracy Lab
## V03 People Movement Behavior Lab
## V04 Short Range Radar Lab
## V09 Long Range People Detect Lab
## V12 3D People Counting Lab


nVidia
https://medium.com/%40mbonsign/complete-guide-for-nvidia-rtx-5070-ti-on-linux-with-pytorch-358454521f04

Notes01:


# Notes - 2025/07/28

## ① BED : 4 Coners Installation

- ⭐ **in JSON:** require parameters (center_x, center_y, rotate_angle)  
- ⭐ **Height (H):** 2.0 m  
- ⭐ **Corners:** 4 (antenna installed on BED corners)
- ⭐ **Status:** checked OK (without retrain)

---

## ② FDS : Rule or AI Mode Selection (in JSON)

- ⭐ **Rule AI Mode Selection: (in JSON)**
  ```
  {
	  "options" : ["Rule", "AI", ".", "..", "..."],  
	  "bitmask" : [1,       1,    0,   0,    0]
  }
  ```
---

## ③ FDS : Multiple Models Selection (in JSON)
- ⭐ **Multiple Model Selection: (example)** 

 ```
	{
	  "mmWave": {
	    "model": {
	      "model_name_v": ["V01_fast_falling", "V02_slow_falling", "V03_sit_falling"],
	      "model_weight_v": [
	        ["./model/my_model_V01_.h5", "./model/my_model_weights_V01_.h5"],
	        ["./model/my_model_V02_.h5", "./model/my_model_weights_V02_.h5"],
	        ["./model/my_model_V03_.h5", "./model/my_model_weights_V03_.h5"]
	      ],
	      "model_bitmask_v": [1, 0, 1]
	    }
	  }
	}
 ```

---

## ④ BED : new request (for alert case need train)

- ⭐ **Alert Condition :** 1/3 Leg or Hand out of BED

---

## ⑤ FDS: request for deployment (for h=2.0m need train)
 ```
  - ⭐ (1) height: 2.4 m for Living Room
           tilt: 45 degree
  
  - ⭐ (2) height: 2.0 m for Toilet Room (Train required)
           tilt: 35 degree 
 ```
---

## ⑥ FDS :  request for SLOW FALLING (need Train)

- ⭐ **Status:**  for patient slow falling case (need train)


---
