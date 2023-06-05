# predicting_person_age

# Dataset Description
## Description
Data는 얼굴 이미지(200x200)와 각 이미지에 대한 Class로 구성이 되어 있습니다.   
Class는 다음과 같습니다.

`0` : 1세 ~ 10세    
`1` : 11세 ~ 20세    
`2` : 21세 ~ 30세    
`3` : 31세 ~ 40세    
`4` : 41세 ~ 50세    

추가적으로, Class를 제외한, 나이(Age), 성별(Gender), 인종(Race)에 대한 정보가 이미지의 이름으로 주어집니다.
자세한 내용은 Dataset과 Testset에서 확인하세요.

## Files   
* **dataset** - 학습을 위해 사용할 이미지 폴더   
* **data.csv** - dataset에 대한 정보가 요약된 csv파일   
* **testset** - test를 위해 사용할 이미지 폴더   
* **testdata.csv** - testset에 대한 정보가 요약된 csv파일   
   
## Dataset   
모델 학습을 위한 이미지 파일들 입니다.   
**dataset**은 Class폴더로 구성이 되어 있습니다.   
각 Class의 이미지는 다음 이름 형식을 따릅니다.   
`[age]_[gender]_[race]_[date&time].jpg`   
   
**age**: 이미지의 정확한 나이   
**gender**: 이미지의 성별로, 0(남자) or 1(여자)   
**race**: 인종으로, 0(백인), 1(흑인), 2(아시아인), 3(동남아인), 4(그외, 히스페닉, 라틴, 중동…)   
**date&time** : 이미지가 생성된 날짜(yyyymmddHHMMSSFFF)   
   
   
> **주의 사항**   
> 각 이미지의 정보만을 사용해서 모델을 구성해도 됩니다.   
> 다만, 추가적인 정보를 제공하여 모델의 성능을 향상시키는 것도 가능합니다. (예를 들어 gender, race)   
> **특히** 학습을 위한 Dataset에는 age정보가 포함되어 있지만, Testset에는 제공이 되지 않습니다.   
> 어떤 모델이 더 좋고, 나쁜지에 대한 판단은 본인이 직접 해보고 내리시길 바랍니다.   
   
## Dataset.csv   
총 7340개의 이미지 파일과 특징들이 제공됩니다.   
***해당 `.csv`파일을 제공하는 이유는 추가적인 특징들을 쉽게 사용하기 위함입니다.***   
   
* `Image` - 파일 이름   
* `Label` - 해당하는 Class   
* `Age` - 해당하는 Age   
* `Gender` - 해당하는 Gender   
* `Race` - 해당하는 Race   
   
## Testset   
모델의 성능을 검증하기 위한 이미지 파일 입니다.   
각 이미지 파일은 다음과 같은 이름 형식을 따릅니다.   
`[gender]_[race]_[date&time].jpg`   
   
* **gender**: 이미지의 성별로, 0(남자) or 1(여자)   
* **race**: 인종으로, 0(백인), 1(흑인), 2(아시아인), 3(동남아인), 4(그외, 히스페닉, 라틴, 중동…)   
* **date&time** : 이미지가 생성된 날짜(yyyymmddHHMMSSFFF)   
   
   
> **주의 사항**   
> 이미지의 나이를 예측하는 문제이기 때문에 age에 대한 정보는 제공되지 않습니다.   
> 다만, gender와 race에 대한 정보는 동일하게 제공되기 때문에 모델 성능 향상에 사용될 수 있습니다.  
   
## Testset.csv   
총 822개의 이미지 파일과 특징들이 제공됩니다.   
   
***해당 `.csv`파일을 제공하는 이유는 추가적인 특징들을 쉽게 사용하기 위함입니다.***   
   
* `Image` - 파일 이름   
* `Gender` - 해당하는 Gender   
* `Race` - 해당하는 Race   
