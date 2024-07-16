# 항공 데이터베이스 구축 및 웹을 활용한 시각화

*   Motivation : 항공 교통 서비스에 대한 지속적인 수요 증가로 인해 항공기 지연 및 취소로 인한 승객들의 불편도 증가
*   목표 :  과거 항공편 데이터를 기반으로 공항, 항공사 및 지연 원인과 같은 다양한 요인에 따른 항공기 지연을 분석 & 분석 결과에 따라 지연의 확률 및 정보 시각화
*   기대효과 : 과거 항공편 데이터를 더 직관적이고 효율적으로 보여줌으로써 사용자 혜택을 증가시키고 항공사 및 공항의 효율성과 비용 효과성 증대


## 기술 스택

![image](https://github.com/user-attachments/assets/6669550b-46bb-47fa-b362-f298f6a8879b)


## 데이터셋
데이터셋 : 17년 1월부터 19년 6월까지의 국내 항공 데이터

![image](https://github.com/user-attachments/assets/ed9223f5-0f6b-4072-bbfc-a61d92818275)


## 데이터 전처리
MySQL을 사용해 전처리 진행 및 Tableau에 데이터 전달

![image](https://github.com/user-attachments/assets/394669d5-e808-4bee-adb9-46cbd3d0f787)
*   분석을 위해 메타 데이터가 담긴 테이블 merge

![image](https://github.com/user-attachments/assets/33dfabdc-c3be-49e3-9400-92605f0a709d)
*   예상 출발 시간, 예상 도착 시간, 실제 도착 시간을 이용해 'Scheduled Time'과 ‘Actual Time’ 계산

![image](https://github.com/user-attachments/assets/214d48b7-5f19-443b-a5bd-b8c1dbff1f0d)
*   'Scheduled Time'과 ‘Actual Time’의 차이를 이용해 'Delay Time' 계산 후 이를 구간화



## Web Programming & Database
* PHP와 Ajax를 사용해 MySQL 데이터베이스에 연결 및 통신하며, 시각화 결과를 웹페이지로 출력

### 웹페이지 구조도
![image](https://github.com/user-attachments/assets/84e9ec93-9cc7-4bcd-8e7f-bc51f4598c3c)


### index.php
![image](https://github.com/user-attachments/assets/af46c626-ca77-4bf7-9328-a1d53bbfb350)
*   'index.php'에서 보여지는 출-도착 공항 및 출발월일은 'data.php'에서 존재하는 데이터만 보이도록 필터링 진행 
