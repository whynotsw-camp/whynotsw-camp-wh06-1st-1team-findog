# 프로젝트 기획서
### :dog:팀명 : 댕댕매칭소

### :raising_hand:팀원

| **김예솔** | **김채린** | **권동현** |
|:--:|:--:|:--:|
|![dog1](https://github.com/whynotsw-camp/whynotsw-camp-wh06-1st-1team-findog/blob/main/image/dog1.jpg)|![dog2](https://github.com/whynotsw-camp/whynotsw-camp-wh06-1st-1team-findog/blob/main/image/dog3.jpg)|![dog3](https://github.com/whynotsw-camp/whynotsw-camp-wh06-1st-1team-findog/blob/main/image/dog2.jpg)|
| 서비스 플로우,<br>시스템 아키텍쳐 설계 | 발표 자료 제작,<br>UI 디자인 | DB ERD,<br>데이터 수집 및 가공 |


### :book: 프로젝트 일정

| **일정** | **내용** | 
|:--:|:--:|
| **1개월차** |서비스 기획 및 아이디어 구체화<br>시스템 아키텍쳐 설계 및 DB 설계|
| **2~5개월차** |UI 디자인 및 프로토타입 개발<br>기능 개발 및 통합|
| **6개월차** |어플리케이션 개발 및 최적화<br>사용자 테스트 및 발표 준비|


---


## :pushpin: 프로젝트 정의
### :ballot_box_with_check: **프로젝트명** : 다시만나개

### :ballot_box_with_check: **목표** 

- 분실 동물 이미지 기반 검색
- 사용자 라이프스타일 맞춤형 품종 추천
- 기존 노출 시스템 개선

### :ballot_box_with_check: **기획 배경**

- 반려동물 양육 인구의 지속적 증가
- 높은 보호소 내 사망률

### :ballot_box_with_check: **시장 및 환경 분석**

- 반려동물 산업 규모 증가 및 긍정적 전망

- 반려동물 관련 소셜 미디어 언급량 증가

- 반려동물 관련 앱 사용자 연령대 확대


---


## :pushpin: 서비스 개요


### :ballot_box_with_check: **기존 서비스의 한계**

[![포인핸드](https://github.com/whynotsw-camp/whynotsw-camp-wh06-1st-1team-findog/blob/main/image/hand.png)](https://pawinhand.kr/)

- **방대한 데이터로 인한 사용자 피로도 증가**
- **비효율적인 노출 구조**
- **사용자 특성을 반영하지 못한 입양 추천**
- **특정 개체 인기 편중 현상**


### :ballot_box_with_check: **핵심 차별화 전략**

| **항목** | **내용** |
|:--:|:--:|
| **사진 기반<br>분실동물 검색** | AI가 사진 속 동물의 특징을 분석하여 유사한<br>분실·보호 동물을 자동으로 매칭해주는 검색 시스템 |
| **개체 노출<br>구조 개선** | 공고 마감이 임박한 동물을 우선적으로 노출해<br>구조 기회를 높이는 시스템 |
| **사용자 선호도<br>기반 품종 추천** | 간단한 질문 응답을 통해 사용자 라이프스타일에 맞는 강아지 품종을 추천해주는 서비스 |
| **사용자 성향 기반 유기견 추천** | 라이프스타일에 맞춰 보호소에 있는 유기견 중<br>어울리는 개체를 추천해주는 서비스 |

### :ballot_box_with_check: **기대 효과**

| **항목** | **기대 효과**|
|:--:|:--:|
| **사용자 만족도 향상** | 맞춤형 서비스 제공으로 사용자 피로도 감소|
| **분실동물 재회율 향상** | 사진 기반 검색으로 빠르고 정확한 재회 지원 |
| **유기동물 입양률 증가** | 맞춤형 추천과 노출 시스템 개선으로 입양률 향상 |
| **보호소 과부화 문제 개선**| 입양 촉진을 통해 보호소 과부화 해소 |


---


## :pushpin: 프로젝트 설계


### :wrench: **기술 스택**
![사용스택](https://github.com/whynotsw-camp/whynotsw-camp-wh06-1st-1team-findog/blob/main/image/drawio_2.png)


---


### :hammer: **시스템 아키텍쳐**

![시스템아키텍쳐](https://github.com/whynotsw-camp/whynotsw-camp-wh06-1st-1team-findog/blob/main/image/drawio_1.png)


---


### :mag_right: **전체 서비스 플로우**

![서비스플로우](https://github.com/whynotsw-camp/whynotsw-camp-wh06-1st-1team-findog/blob/main/image/image3.jpg)


---


### :pencil: **데이터 선정**

| **데이터**  | **출처** | **데이터<br>형태** | **활용 방안** |
|:--:|:--:|:--:|:--:|
|분실동물 조회<br>서비스| 농림 축산<br>식품부 | OpenAPI| 분실 동물 등록 시<br>보호소 동물과 유사도 분석 후 자동 추천 및 보호소 정보 제공 |
|입양 대기동물 현황| 서울 동물<br>복지지원센터 | csv | 사용자가 분실 동물 정보 등록 시<br>연동된 보호소 동물과 유사한 동물을 자동 추천 및 입양대기 데이터와 매칭하여 보호소 정보 제공 |
|스탠포드 120종 강아지| Kaggle | csv | 선호도 검사 결과를 가지고<br> 품종 데이터와 영상 데이터를 학습 모델을 활용해 강아지 품종 추천 |
|반려동물 구분 동물 영상| AI Hub | OpenAPI | 선호도 검사 결과를 바탕으로<br>품종 이미지과 영상 데이터를 학습한 모델을 활용해 강아지 품종 추천 |


---


### :file_folder: **DB - ERD**

[테이블정의서](https://github.com/whynotsw-camp/whynotsw-camp-wh06-1st-1team-findog/blob/main/%ED%85%8C%EC%9D%B4%EB%B8%94%20%EC%84%A4%EB%AA%85%EC%84%9C.pdf)

![ERD](https://github.com/whynotsw-camp/whynotsw-camp-wh06-1st-1team-findog/blob/main/image/erd.png)
![ERD2](https://github.com/whynotsw-camp/whynotsw-camp-wh06-1st-1team-findog/blob/main/image/erd2.png)


---

    


