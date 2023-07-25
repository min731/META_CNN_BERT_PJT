# 📖 프로젝트명

### ✔️ 실시간 얼굴 인식을 통한 맞춤형 광고 제공 프로젝트 (메티버스 아카데미 2기 AI반 딥러닝 팀 프로젝트)

# 📃 프로젝트 소개

### ✔️ MediaPipe, CNN)을 활용한 실시간 얼굴 인식을 통한 맞춤형 광고 제공 프로젝트입니다.  

(주제 선정 배경, 개요 등)

# 👩‍🔧 팀원 소개 및 역할

### ✔️ 팀원
메타버스 아카데미 2기 AI반 김명진, 여형구, 임정민, 김해니 총 4명

### ✔️ 역할 분담

주제 선정 : 모든 팀원

데이터 서치/수집 : 김해니

데이터 전처리 : 임정민

Face Recognition 모델 테스트 :

🔹FaceNet(MTCNN) - 여형구, 임정민<br>
🔹MediaPipe - 김명진, 김해니<br>

CNN 모델링 :

🔹EfficientNetB0 - 김명진<br>
🔹ResNet50 - 여형구<br>
🔹DenseNet121 - 임정민<br>
🔹VGGNet16 - 김해니<br>

평가 지표 비교/분석 : 김명진

발표 준비 및 PT 발표 : 여형구

# 📅프로젝트 진행 기록

### ✔️ 수행 기간
2023.07.17 ~ 2023.07.21

### ✔️ 세부 진행 기록
- 23-07-17 (9:00 ~ 18:00) : 아이디어 팀회의/피드백, 주제 선정, 데이터 서치
- 23-07-18 (9:00 ~ 14:00) : 각도별 안면 데이터 수집, DataFrame 활용 Multi-Label 형식 전처리
- 23-07-18 (14:00 ~ 20:00) : Face Recognition 
- 23-07-05 (9:00 ~ 15:00) : Pytorch 활용 AlexNet, ResNet34, VGG16 모델 학습
- 23-07-05 (15:00 ~ 20:00) : Tensorboard 활용 평가 지표 비교(Accuarcy,Loss), 실전 데이터 Evaluate 원인/결과/개선점 분석
- 23-07-06 (9:00 ~ 12:00) : AI 전공 내부 PPT/대본 작성, 블로그/깃허브 정리
- 23-07-06 (13:00 ~ 18:00) : AI 전공 내부 PT 발표 및 질의응답

++
- 23-07-13 : Tag2Text 모델 도입, Pretrained된 Tag2Text 모델 활용 Evaluate, 평가 지표 확인
- 23-07-14 : 전 전공 PT 발표 및 질의응답


# 📊 데이터 소개
### ✔️ Dacon '데이콘 Basic 자동차 가격 예측 AI 경진대회' 데이터셋을 활용하였습니다.
[데이콘 Basic 자동차 가격 예측 AI 경진대회](https://dacon.io/competitions/official/236114/overview/description) <br><br>

![image](https://github.com/woojooc/ML_Car/assets/115389344/66e2a813-ab89-4802-92a7-8d49f6fe1173)


### ✔️ 데이터 세부 사항
데이터 갯수 : 57920개<br>
ID : 샘플 별 고유 id<br>
생산년도 : 차량이 생산된 연도<br>
모델출시년도 : 차량의 모델이 처음으로 출시된 연도<br>
브랜드<br>
차량모델명<br>
판매도시 : 3글자로 인코딩된 도시 이름<br>
판매구역 : 3글자로 인코딩된 구역 이름<br>
주행거리 : 총 주행 거리(km)<br>
배기량 : 내연기관에서 피스톤이 최대로 밀어내거나 빨아들이는 부피 (cc)<br>
압축천연가스(CNG) : 압축천연가스(CNG) 자동차 여부<br>
경유 : 경유 자동차 여부<br>
가솔린 : 가솔린 자동차 여부<br>
하이브리드 : 하이브리드 자동차 여부<br>
액화석유가스(LPG) : 액화석유가스(LPG) 자동차 여부<br>
가격 : 자동차 가격(백만원)<br>

# 💡 주요 내용

### ✔️ 사전 학습

주제 선정 배경
1. 요즘 스마트폰, 인터넷은 검색 기록, 영상 시청 정보를 바탕으로 개인화된 광고를 추천해주고 있음<br>
   (1) 사람들은 출퇴근, 이동 시에 대중 교통을 이용하며 지하철 광고, 버스 정류장 광고를 보게 됨<br>
   (2) 광고 효과를 높이기 위해 지하철, 버스정류장 광고도 맞춤형으로 제공<br>
   (3) 검색 기록, 영상 기록을 확인할 수는 없으니 안면 인식을 통해 맞춤형 광고를 제공<br>
2. 광고주(기업) 입장에서 광고 효과는 높이되 비용을 줄이길 원함<br>
   (1) 광고 효과를 높이고 비용을 줄이기 위해서 성별, 연령대를 예측해서 실제 수요가 있을 것 같은 사람들에게 광고 제공<br>

도메인 학습
1. 국내/해외별 중고차 시장 가격 영향 요인이 다를 것이라 예상
2. 국내 중고 자동차 시장 가격 영향 요인 : 연식, 주행거리(km), 배기량(CC), 마력 순
3. 해외(튀르키예) 중고 자동차 시장 가격 영향 요인 : 브랜드, 주행거리(km), 연식, 변속기 순

### ✔️ 개요

1. 차량 번호를 조회하여 중고차 시세를 예측하는 서비스의 머신러닝 모델 기획
2. 소셜 데이터에 기반한 중고차 매매 관련 외부요인 탐색<br>
   (1) 크롤링/워드 클라우드 활용 네이버 블로그 '중고차,'중고차 하락' 검색 시 '수출','시세','사고','폐차','업체','국내' 등 키워드 도출
   (2) 해외 기준 국내 중고차 품질의 우수함을 인정받고 있지만 시스템의 부재로 걸맞는 가격을 받지 못하는 상황

### ✔️ 딥 러닝

1. 데이터 전처리<br>
   (1) 신차 / 중고차 분리 : 주행거리 < 200km 의 신차 데이터 drop<br>
   (2) 이상치 데이터 제거 : 주행거리 >= 250만km (최댓값) 데이터 1개 관측/제거<br>
   (3) 중복 Feature 통합 : get_dummies화된 연료 유형 통합<br>
   (4) 불필요한 컬럼 제거 : 'ID'(데이터 고유 키값) , 'City','Area' : 모두 폴란드 지역/도시<br>
   (5) 문자형 데이터 변환 : '브랜드','차량모델명','판매도시','판매구역' Label Encoding<br>
   (6) (선택사항) MinMaxScaling : '연도','차량모델출시년도' MinMaxScaler 적용<br>
2. 학습 결과 (MAE) <br>
   (1) LightGBM : 6.8398<br>
   (2) RandomForest : 6.3714 (K-fold,cv=5,avg값 기준)<br>
   (3) XGBoost : 6.4092<br>
   (4) LinearRegression : 11.95<br>
   (5) Lasso/LassoCV : 13.44 (alpha=1)<br>

    💡MAE 기준 가장 낮은 RandomForest 의 Feature_importances : '생상년도','CC','주행거리','차량출시년도'

3. AutoML <br>

   (1) 앞서 구현한 모델들의 MAE값을 줄이기 위해 Optuna, Auto Gluon, Pycaret 총 3가지의 AutoML을 사용<br>
   (2) Optuna : xgb의 경우 best Trial의 값이 5.885, lgbm의 경우 best trial의 값이 5.9726으로 기존의 MAE값 보다 더 나은 결과를 도출<br>
   (3) Auto Gluon :  L2 모델이 6.051919, xgb는 6.245744, lgbm은 6.165254로 기존의 MAE값 보다 더 나은 결과를 도출<br>
   (4) Pycaret : Blending을 통해 여러 모델들을 혼합하여 새로운 모델 생성 -> MAE가 가장 낮게 나온 모델인 CatBoost, XGBoost 모델 Blending : 5.8961, 렌덤으로 Blending
       한 모델 :  5.9002, 기존의 MAE 값 보다 더 나은 결과 도출<br>
   (5) 결론적으로 AutoML을 사용한 결과 모든 프레임 워크들이 기존의 K-Fold된된 모델의 MAE값보다 확연히 낮아진것을 확인하였으며, 그 중에서도 Optuna를 통해 생성한              XGBoost 모델의 MAE값이 가장 좋게 나온 것을 확인<br>

4. Auto ML 학습 결과 (MAE) <br>
   (1) Optuna (XGBoost) : 5.885<br>
   (2) Auto Gluon (L2) : 6.051919<br>
   (3) Pycaret (CatBoost, XGBoost Blend 모델) : 5.8961<br>
   

### ✔️ 결과

1. 이번 수입 중고차 가격 예측 프로젝트에서 MAE 기준 가장 최적화된 모델은 Optuna(AutoML)의 XGBoost 모델이고 '생산년도','주행거리','배기량','차량모델' 순으로 가격에 영향을 미쳤습니다.
2. 금리,나라별 가격,업체(딜러) 등을 독립변수로 추가할 수 있다면 더욱 정확한 예측 가능합니다.
3. 해당 모델/서비스를 통해 중고차 구매차 및 판매자들에게 여 중고치 시장의 활성화를 도모할 수 있습니다.

# 🛠 기술 스택

### ▪ 언어
<img src="https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white">

### ▪ 주요 라이브러리
<img src="https://img.shields.io/badge/scikit learn-F7931E?style=for-the-badge&logo=scikit learn&logoColor=white"> <img src="https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white">
<img src="https://img.shields.io/badge/numpy-013243?style=for-the-badge&logo=numpy&logoColor=white"> <img src="https://img.shields.io/badge/seaborn-99CC00?style=for-the-badge&logo=seaborn&logoColor=white"> <img src="https://img.shields.io/badge/matplotlib-0058CC?style=for-the-badge&logo=matplotlib&logoColor=white"> <img src="https://img.shields.io/badge/wordcloud-FF4F8B?style=for-the-badge&logo=wordcloud&logoColor=white">
<img src="https://img.shields.io/badge/konlpy-FF0000?style=for-the-badge&logo=konlpy&logoColor=white"> <img src="https://img.shields.io/badge/collections-7FADF2?style=for-the-badge&logo=collections&logoColor=white">

### ▪ 개발 툴
<img src="https://img.shields.io/badge/VS code-2F80ED?style=for-the-badge&logo=VS code&logoColor=white"> <img src="https://img.shields.io/badge/Google Colab-F9AB00?style=for-the-badge&logo=Google Colab&logoColor=white">

### ▪ 협업 툴
<img src="https://img.shields.io/badge/Github-181717?style=for-the-badge&logo=Github&logoColor=white"> <img src="https://img.shields.io/badge/Google Slides-FFBB00?style=for-the-badge&logo=Google Slides&logoColor=white">

# 🔍 참고 자료
### ✔️ 데이터
  
[데이콘 Basic 자동차 가격 예측 AI 경진대회](https://dacon.io/competitions/official/236114/overview/description)

### ✔️ 논문
1) 고찬영, 2021, 다중선형회귀분석을 이용한 중고차 가격 예측 연구 : A사의 사례를 중심으로』, 인하대학교 물류전문대학원 석사학위 논문
2) Sümeyra MUTİ1, Kazım YILDIZ2, 2023, Using Linear Regression For Used Car Price Prediction
,International Journal of Computational and
Experimental Science and ENgineering
,Vol. 9-No.1 (2023) pp. 11-16

