
<img src="https://github.com/2814894078/Causal-NCD/blob/main/Fig%201.png" width="600px">

​**Figure 1.** The optimization curve of the loss in Eq. (8) .

<img src="https://github.com/2814894078/Causal-NCD/blob/main/Fig%202.jpg" width="1000px" >

**Figure 2.** Distribution plot of the SemanticKITTI、SemanticPOSS and Harder SemanticPOSS dataset. 

<img src="https://github.com/2814894078/Causal-NCD/blob/main/Fig%203.png" width="800px" >

**Figure 3.** The training dynamics of the threshold θ and the mIoU of the novel class segmentation on the SemanticPOSS and SemanticKITTI dataset.



**Table 1.** Comparison of computational complexity of different methods on the SemanticPOSS dataset.

|                       | NOPS  | DASL  | Ours  |
| --------------------- | ----- | ----- | ----- |
| Training Time (hours) | 11.41 | 20.76 | 21.69 |
| Test Time (hours)     | 0.46  | 0.90  | 1.03  |
| GPU memory (GB)       | 11    | 23.02 | 23.68 |

**Table 2.** Comparison of computational complexity of different methods on the SemanticKITTI dataset.

|                       | NOPS  | DASL   | Ours   |
| --------------------- | ----- | ------ | ------ |
| Training Time (hours) | 28.68 | 153.04 | 160.35 |
| Test Time (hours)     | 0.98  | 2.56   | 3.22   |
| GPU memory (GB)       | 18.19 | 34.37  | 35.49  |



**Table 3.** Detailed results for SemanticPOSS.

| Method | Head | Medium | Tail |
| ------ | ---- | ------ | ---- |
| NOPS   | 37.5 | 21.9   | 4.4  |
| DASL   | 45.0 | 30.8   | 11.2 |
| Ours   | 40.3 | 48.5   | 11.4 |

**Table 4.** Detailed results for SemanticKITTI.

| Method | Head | Medium | Tail |
| ------ | ---- | ------ | ---- |
| NOPS   | 26.1 | 28.3   | 7.4  |
| DASL   | 33.8 | 32.2   | 8.5  |
| Ours   | 31.0 | 33.4   | 11.4 |



**Table 5.** Original SemanticKITTI splits, defined as KITTI-nⁱ, where n is the number of novel classes and i is the split index.

|  Split   |                    Novel Classes                     |
| :------: | :--------------------------------------------------: |
| KITTI-5⁰ |    building, road, sidewalk, terrain, vegetation     |
| KITTI-5¹ |       car, fence, other-ground, parking, trunk       |
| KITTI-5² | motorcycle, other-vehicle, pole, traffic-sign, truck |
| KITTI-4³ |       bicycle, bicyclist, motorcyclist, person       |

**Table 6.** Original SemanticPOSS splits, defined as POSS-nⁱ, where n is the number of novel classes and i is the split index.

|  Split  |         Novel Classes         |
| :-----: | :---------------------------: |
| POSS-4⁰ | building, car, ground, plants |
| POSS-3¹ |      bike, fence, person      |
| POSS-3² |   pole, traffic-sign, trunk   |
| POSS-3³ |  cone-stone, rider, trashcan  |

**Table 7.** Harder setting of SemanticPOSS dataset.

|           Split           |                       Novel Classes                        |
| :-----------------------: | :--------------------------------------------------------: |
| Harder POSS-6<sup>1</sup> |        building, car,  person,cone-stone,pole,trunk        |
| Harder POSS-7<sup>2</sup> | bike, fence, traffic-sign, plants, ground, rider, trashcan |

**Table 8:** Harder splits results on SemanticPOSS dataset. The class corresponding to the column where the bolded results are located is the novel class. 

|           Split           | Method |   bike   |  build.  |   car    |  cone.  |  fence   |  grou.   |  pers.   |  plants  |   pole   |  rider  |  traf.   | trashc. |  trunk   |  Novel   | Known | All  |
| :-----------------------: | :----: | :------: | :------: | :------: | :-----: | :------: | :------: | :------: | :------: | :------: | :-----: | :------: | :-----: | :------: | :------: | :---: | :--: |
|                           |  Full  |   48.3   |   86.9   |   57.2   |  38.5   |   49.8   |   79.1   |   63.8   |   81.7   |   37.0   |  58.1   |   33.5   |   9.1   |   27.4   |    -     |   -   | 51.5 |
| Harder POSS-6<sup>1</sup> |  NOPS  |   37.4   |   22.9   |   8.1    |   0.0   |   30.3   |   78.9   |   4.8    |   72.9   |   1.0    |  42.9   |   25.8   |   9.2   |   9.6    |   7.7    | 42.5  | 26.5 |
|                           |  DASL  |   46.0   |   26.1   |   27.5   |   2.8   |   46.9   |   77.6   |   35.0   |   77.8   |   0.2    |  58.6   |   30.5   |   3.2   |   0.0    |   15.3   | 48.7  | 33.2 |
|                           |  Ours  |   51.1   | **34.6** | **34.3** | **8.9** |   44.9   |   80.8   | **46.1** |   77.9   | **11.0** |  61.6   |   35.4   |   5.4   | **14.7** | **24.9** | 51.0  | 40.0 |
| Harder POSS-7<sup>2</sup> |  NOPS  |   6.1    |   71.3   |   35.6   |  21.2   |   3.1    |   42.9   |   44.5   |   26.0   |   24.4   |   0.7   |   0.6    |   0.1   |   24.8   |   11.4   | 37.0  | 23.2 |
|                           |  DASL  |   26.3   |   82.0   |   51.4   |  18.0   |   10.4   |   40.0   |   67.5   |   32.5   |   31.2   |   0.0   |   6.3    |   0.0   |   11.7   |   16.5   | 44.5  | 29.4 |
|                           |  Ours  | **29.8** |   88.4   |   56.6   |  22.1   | **29.2** | **49.6** |   71.9   | **41.4** |   34.0   | **8.9** | **10.5** | **4.3** |   17.1   | **24.8** | 48.4  | 35.7 |


**Table 9.** Low similarity setting of SemanticPOSS dataset. 

| Split |                        Novel Classes                         |
| :---: | :----------------------------------------------------------: |
|   1   | building, fence, cone-stone, pole, traffic-sign, trashcan, ground |
|   2   |           car, bike, rider, person, trunk, plants            |



**Table 10.** Low similarity setting results on SemanticPOSS dataset. 

| Split | Method |  Novel   | Known | All  |
| :---: | :----: | :------: | :---: | :--: |
|   1   |  NOPS  |   4.1    | 41.4  | 22.8 |
|       |  DASL  |   12.6   | 45.7  | 29.2 |
|       |  Ours  | **17.8** | 46.1  | 32.0 |
|   2   |  NOPS  |   7.4    | 42.8  | 25.1 |
|       |  DASL  |   18.0   | 50.2  | 34.1 |
|       |  Ours  | **27.3** | 52.5  | 39.9 |


