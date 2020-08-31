# Bio-ASP Lab Evaluation Metrics

## Perceptual Evaluation of Speech Quality (PESQ)

### pypesq:  
https://github.com/vBaiCai/python-pesq

PESQ score:  
* Narrow Band – Raw MOS  

datatype: int / float  
  
  
  
    
### PESQ - P.862  
Reference implementation for ITU-T Recommendations P.862, P.862.1 and P.862.2.
Version 2.0 October 2005.  

* Mac: PESQ_MAC.bin  
* Linux: PESQ  
* Windows: pesq.exe  

PESQ score:
* Narrow Band  – Raw MOS, MOS LQO  
* Wide Band    – MOS LQO  

datatype: **int16**  


### Restults: 

Testing data: TMHINT
- Normal: noisy speech
- Cut: 1~10% shorter
- Expand: 1~10% longer (edge)
- Scale: ×0.6
- noise: noises (takeoff.wav)

#### pypesq:
|Data type |          |Normal         |Scale          |Noise          |Expand         |Cut            |  
|:---------|:---------|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|
| clean    | noisy    |               |               |               |               |               |
| float32  | float32  | 1.871         | 1.871         |1.229          |X              |X              |
| int16    |float32   | 1.732         |   1.541       |1.213          |X              |X              |
| int16    |int16     | 1.866         |    1.870      |1.238          |X              |X              |


#### P.862 - MacOS  
|                    |Normal         |Scale          |Noise          |Expand         |Cut            |  
|:-------------------|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|
| NB - Raw MOS       | 1.865         | 1.871         |1.233          |1.848          |1.815          |
| NB - MOS LQO       | 1.572         |   1.577       |1.303          |1.561          |1.539          |
| WB - MOS LQO       | 1.191         |    1.199      |1.162          |1.186          |1.183          |

  
#### P.862 - linux  
|                    |Normal         |Scale          |Noise          |Expand         |Cut            |  
|:-------------------|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|
| NB - Raw MOS       | 1.865         | 1.871         |1.233          |1.848          |1.815          |
| NB - MOS LQO       | 1.572         |   1.577       |1.303          |1.561          |1.539          |
| WB - MOS LQO       | 1.191         |    1.199      |1.162          |1.186          |1.183          |


  
#### P.862 - Windows
|                    |Normal         |Scale          |Noise          |Expand         |Cut            |  
|:-------------------|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|
| NB - Raw MOS       | 1.842         | 1.797         |1.183          |1.825          |1.790          |
| NB - MOS LQO       | 1.552         |   1.518       |1.267          |1.541          |1.518          |
| WB - MOS LQO       | 1.162         |    1.135      |1.150          |1.158          |1.158          |


#### summary
Narrow Band – Raw MOS (int16)

|                    |Normal         |Scale          |Noise          |Expand         |Cut            |  
|:-------------------|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|
| pypesq             | 1.866         | 1.870         |1.238          |X              |X              |
| P.862 - MacOS      | 1.865         |   1.871       |1.233          |1.848          |1.815          |
| P.862 - linux      | 1.865         |    1.871      |1.233          |1.848          |1.815          |
| P.862 - Windows    | 1.842         |    1.797      |1.183          |1.825          |1.790          |





## Short-Time Objective Intelligibility (STOI)  

