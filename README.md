# 📖 프로젝트명

### ✔️ 실시간 얼굴 인식을 통한 맞춤형 광고 제공 프로젝트(메티버스 아카데미 2기 AI반 딥러닝 팀 프로젝트)

# 📃 프로젝트 소개

### ✔️ MediaPipe, CNN (Transfer Learning)을 활용한 실시간 얼굴 인식을 통한 맞춤형 광고 제공 프로젝트입니다.  

(주제 선정 배경, 개요 등)

# 👩‍🔧 팀원 소개 및 역할

### ✔️ 팀원
메타버스 아카데미 2기 AI반 김명진, 여형구, 임정민, 김해니 총 4명

### ✔️ 역할 분담

주제 선정 : 모든 팀원

데이터 서치/수집 : 김해니

데이터 전처리 : 임정민

OpenCV 활용 카메라(웹캠) 모듈 테스트 : 여형구, 김해니 

Face Recognition 모델 테스트 :

🔹FaceNet(MTCNN) - 여형구, 임정민<br>
🔹MediaPipe - 김명진, 김해니<br>

CNN 모델링 :

🔹EfficientNetB0 - 김명진<br>
🔹ResNet50 - 여형구<br>
🔹DenseNet121 - 임정민<br>
🔹VGGNet16 - 김해니<br>

CNN 평가 지표 비교/분석 : 김명진

카메라/Face Recognition/CNN 모듈 통합 : 김명진, 임정민

발표 PPT 및 대본 작성 : 모든 팀원  

PT 발표 : 여형구

# 📅프로젝트 진행 기록

### ✔️ 수행 기간
2023.07.17 ~ 2023.07.21

### ✔️ 세부 진행 기록
- 23-07-17 : 아이디어 팀회의/피드백, 주제 선정, 데이터 서치
- 23-07-18 (9:00 ~ 14:00) : cv2 활용 카메라(웹캠) 테스트, 각도별 안면 데이터 수집
- 23-07-18 (14:00 ~ 20:00) : DataFrame 활용 Multi-Label 형식 전처리 
- 23-07-19 : 안면 인식을 위한 MediaPipe, FaceNet(MTCNN)모듈 성능 테스트, 카메라(웹캠) 연동 모듈 개발
- 23-07-20 : 팀원별 할당된 전이학습 CNN 모델 Multi-Label 학습, 카메라/Face-Recognition/CNN 분류 통합 모듈 개발
- 23-07-21 (9:00 ~ 12:00): CNN 모델 튜닝 및 재학습, PPT 초안 및 대본 작성
- 23-07-21 (13:00 ~ 22:00): PPT/대본 작성, 블로그/깃허브 정리

  ++
- 23-07-31 : AI 전공 내부 발표 및 질의응답

# 📊 데이터 소개
### ✔️ AI-Hub '가족 관계가 알려진 얼굴 이미지 데이터' 데이터셋의 일부를 활용하였습니다.

![image](https://github.com/haeniKim/ai-project-team4/assets/115389344/842f0c23-673e-462a-8d23-fbe806201144)

[가족 관계가 알려진 얼굴 이미지 데이터](https://aihub.or.kr/aihubdata/data/view.do?dataSetSn=528) <br><br>

### ✔️ 데이터 세부 사항
![image](https://github.com/haeniKim/ai-project-team4/assets/115389344/172f57e4-b179-4e00-9f40-73b0c7b135b5)

- 총 데이터 갯수 : 43850개<br>
- 남녀 비율 각 45%, 55%
- 3014명의 이미지 데이터
- 10대 연령이 27%로 가장 많은 비율 차지
- 40대 연령이 24%로 두번째로 많은 비율 차지
- 여러 각도의 이미지 데이터
- 다양한 밝기/환경의 이미지 데이터


# 💡 주요 내용

### ✔️ 주제 선정 배경 및 개요

(수정중)

### ✔️ 카메라(웹캠) 모듈

1. Opencv 활용 노트북 웹캠 연동
2. 대중교통 / 엘리베이터 탑승 시간을 고려하여 실시간 영상에서 10초에 한번씩 Capture하게 설정
3. 영상에서 캡쳐된 frame을 Face-Recognition 전 BGR2RGB Color 변환

### ✔️ Face-Recognition

1. 안면 검출을 위한 모듈(MediaPipe, FaceNet(MTCNN)) 서치
2. 1920x1080 이미지 데이터 1000개 기준 Inference 속도 비교
3. 짧은 시간 탑승하는 대중교통/엘리베이터 특성 고려 =>  추론 속도 기준 약 3배 빠른 MediaPipe를 프로젝트에 활용

![image](https://github.com/haeniKim/ai-project-team4/assets/115389344/c051b558-d4db-4e09-b34a-f9e789c18d4d)

4. MediaPipe를 활용한 안면 이미지 Crop시, 이목구비까지만 추출되어 저조한 성별 분류 정확도를 보였음  => 추출되는 안면 이미지 frame을 확장하여 얼굴형/헤어 스타일까지 포함되게끔 Crop

### ✔️ CNN Multi-Label 데이터 전처리 

1. 다양한 각도/연령별 안면 데이터가 포함된 'AI-Hub '가족 관계가 알려진 얼굴 이미지 데이터' 활용
2. 해당 데이터에서 전문 스튜디오에서 촬영된 정제된 데이터 제외, 야외에서 촬영된 데이터만 활용
3. Multi-Label을 위한 이미지 데이터별 성별/연령 Labeling (Dataframe 활용)

![image](https://github.com/haeniKim/ai-project-team4/assets/115389344/73b4fe21-2222-4c6b-8cc7-7f5a1973a585)

[Multi-Label 참고 링크](https://vijayabhaskar96.medium.com/multi-label-image-classification-tutorial-with-keras-imagedatagenerator-cd541f8eaf24)

### ✔️ CNN Multi-Label 모델 학습 및 Evaluate Accuaracy

1. EfficientNetB0 (weights='imagenet', epochs=10(Early Stopping), optim=Adam, lr=0.001,batch_size=16), Accuracy = 0.5628
2. VGG16 (weights='imagenet', epochs=10(Early Stopping), optim=Adam, lr=0.001,batch_size=16), Accuracy = 0.8086
3. DenseNet121Net (weights='imagenet', epochs=10(Early Stopping), optim=Adam, lr=0.001,batch_size=16), Accuracy = 0.9432
4. ResNet50 (weights='imagenet', epochs=10(Early Stopping), optim=Adam, lr=0.001,batch_size=16), Accuracy = 0.8702

### ✔️ 성별/연령 분류에 따른 광고 송출

![image](https://github.com/haeniKim/ai-project-team4/assets/115389344/ffa46364-dbac-461b-a341-fb54422ca627)

   
### ✔️ 결과

(수정)

# 🛠 기술 스택

### ▪ 언어
<img src="https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white">

### ▪ 주요 라이브러리
<img src="https://img.shields.io/badge/tensorflow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white"> <img src="https://img.shields.io/badge/pytorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white"> <img src="https://img.shields.io/badge/torchvision-29A7DF?style=for-the-badge&logo=torchvision&logoColor=white"> <img src="https://img.shields.io/badge/opencv-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white"> <img src="https://img.shields.io/badge/MediaPipe-1299F3?style=for-the-badge&logo=MediaPipe&logoColor=white"> <img src="https://img.shields.io/badge/facenetpytorch-FF5500?style=for-the-badge&logo=facenetpytorch&logoColor=white"> <img src="https://img.shields.io/badge/keras-D00000?style=for-the-badge&logo=keras&logoColor=white"> <img src="https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white"> <img src="https://img.shields.io/badge/numpy-013243?style=for-the-badge&logo=numpy&logoColor=white"> <img src="https://img.shields.io/badge/matplotlib-0058CC?style=for-the-badge&logo=matplotlib&logoColor=white"> <img src="https://img.shields.io/badge/pillow-006AFF?style=for-the-badge&logo=pillow&logoColor=white">

### ▪ 개발 툴
<img src="https://img.shields.io/badge/VS code-2F80ED?style=for-the-badge&logo=VS code&logoColor=white"> <img src="https://img.shields.io/badge/Google Colab-F9AB00?style=for-the-badge&logo=Google Colab&logoColor=white">

### ▪ 협업 툴
<img src="https://img.shields.io/badge/Github-181717?style=for-the-badge&logo=Github&logoColor=white"> <img src="https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=Notion&logoColor=white">

# 🔍 참고 자료
### ✔️ 데이터
  
![image](https://github.com/haeniKim/ai-project-team4/assets/115389344/73b4fe21-2222-4c6b-8cc7-7f5a1973a585)

[Multi-Label 참고 링크](https://vijayabhaskar96.medium.com/multi-label-image-classification-tutorial-with-keras-imagedatagenerator-cd541f8eaf24)

### ✔️ 논문
(수정중)

