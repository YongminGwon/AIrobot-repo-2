# 로봇 가족
##### 부제 : AMR과 관제 기술을 이용한 스마트 물류센터 구현 

<br>
<img src="https://user-images.githubusercontent.com/110883172/218902218-3180dd52-6303-4bcb-adc9-3e61bb6fd40e.png" width="200" height="200">

###### 팀원 : 권용민, 김두엽, 류도현, 박민제, 박인, 손훈민, 정재욱, 최선민
<br>
<br>

## 프로젝트 개요
- 20232년 2월 23일 발표된 정부 정책인 '[스마트 물류 인프라 구축방안](https://www.korea.kr/news/visualNewsView.do?newsId=148912027&pWise=sub&pWiseSub=I1)'
<img src="https://user-images.githubusercontent.com/110883172/220928275-43f94830-4d69-4403-b48b-676e44df54b4.png" width="400" height="400">

 국토부는 차세대 물류 서비스 구현, 세계 최고 수준의 물류 네트워크 구축, 첨단기술 기반 물류 안전망 강화를 위해 투자를 하겠다고 발표를 했습니다. 이러한 흐름 속에서 우리 팀은 다음 두가지 키워드에 집중합니다. __차세대 물류 서비스 구현__ 과 __첨단기술 기반 물류 안정망 강화__ .
 
__차세대 물류 서비스 구현__ 을 위해 저희는 __AMR__ 을 한 번 구현해보고자 합니다. 
- 물류센터에는 수많은 AMR 로봇이 필요합니다. 이러한 상황에서 3D Lidar와 같은 고가의 장비없이 __2D Lidar__ 와 __deepth camera__ 만으로 구현을 할 수 있다면 경쟁력이 있을 것입니다.
- 첫 번째 AMR(엄마로봇)은 3D Lidar를 대체하여 deepth camera를 통한 Visual SLAM 작업을 합니다. 그래서 3차원 Map이 필요한 공간에서 작업을 할 수 있습니다. 
- 두 번째 AMR(아기로봇)은 2D Lidar를 통해 통상적인 SLAM 작업을 합니다. 2차원 Map만으로 충분히 작업을 할 수 있는 공간에서 사용할 수 있습니다. 
- 엄마로봇이 물류창고의 특정 구역에 도착하면 아기로봇(AMR)이 출발하여 구역의 이곳저곳을 돌아다니면서 필요한 물품을 가져오거나, 재고를 조사하거나 등등의 역할을 수행한 후 엄마로봇에 집결하고, 엄마로봇은 아기로봇을 태워 다음 구역으로 이동합니다.

  
 



## 프로젝트 목표
#### PART 1. 엄마로봇
- 자율주행 실외 배송로봇 구현
- 라이다를 사용하지 않고 자율주행 구현 (Visual SLAM)

#### PART 2. 아기로봇
- 자율주행 실내 배송로봇 구현
- 2대 이상의 Fleet Management 구현

#### PART 3. 통합 인터페이스 구현
- PART 2의 Fleet Management 관제 소프트웨어 제작
- Unity 엔진을 통한 디지털 트윈 구현




## 프로젝트 구체화
#### PART 1. 엄마로봇 (유비쿼티 MAGNI)
- 이미지 세그멘테이션과 Visual SLAM 기술을 통해 Localization하고, 경로를 생성하여 차로를 따라간다.
- 신호등이나 보행자 등의 객체는 YOLO를 통해서 검출하고, 이 때 피하거나 정지할 수 있도록 한다.

#### PART 2. 아기로봇 (PINKBOT BASED ON ADDBOT)
- 실내용 SLAM 기술과 Localization 기술을 통해 경로를 생성한다.
- 실내에서도 장애물을 회피하거나 정지할 수 있어야 한다. 실내배송로봇이 목적지까지 도달하면 다음 목적지로 이동한다. 이동을 마치면 실외배송로봇으로 복귀를 한다.
- 여러 대의 로봇을 관제하는 Fleet Management를 구현한다.


#### PART 3. 통합 인터페이스 구현
- 실외로봇과 실내로봇을 관제하는 인터페이스가 필요하다. 이는 APP이 될 수 있고, 디지털트윈을 통해 구현할 수도 있다.
- 우선은 Unity를 통해 구현을 할 예정이다.
