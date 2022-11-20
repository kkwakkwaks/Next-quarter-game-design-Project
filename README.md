# 다음 분기에 어떤 게임을 설계해야 할까

**DATA**
 https://ds-lecture-data.s3.ap-northeast-2.amazonaws.com/datasets/vgames2.csv
* Name : 게임의 이름입니다.
* Platform : 게임이 지원되는 플랫폼의 이름입니다.
* Year : 게임이 출시된 연도입니다.
* Genre : 게임의 장르입니다.
* Publisher : 게임을 제작한 회사입니다.
* NA_Sales : 북미지역에서의 출고량입니다.
* EU_Sales : 유럽지역에서의 출고량입니다.
* JP_Sales : 일본지역에서의 출고량입니다.
* Other_Sales : 기타지역에서의 출고량입니다.

![image](https://user-images.githubusercontent.com/99347825/202903450-7cbe0623-0a6c-474b-9313-af31cbf75917.png)
### 1. 지역에 따라서 선호하는 게임 장르가 다를까
![image](https://user-images.githubusercontent.com/99347825/202903507-b737ea37-673e-4227-a991-8c5fcd6f04e2.png)
* 일본에서만 **Role-Playing** 장르가 1위임을 알 수 있다.

![image](https://user-images.githubusercontent.com/99347825/202903604-27d007b9-a279-4031-9c43-aac4391bf472.png)
### => 다음 분기 게임 장르는 네 지역에서 모두 인기 있는 **Action**이나 **Sports** 가 좋을것이라 생각된다.

### 2. 연도별 게임의 트렌드가 있을까
#### 2-1. 장르
![image](https://user-images.githubusercontent.com/99347825/202903693-f3f17784-3f98-482c-9951-39f3db870779.png)
* **1995년 이전**까지는 특별한 양상을 보이지 않다가
**1995년 ~ 2002년** 까지 **Sports** 장르의 게임이 인기 있었고, 
**2003년 ~ 2016년** 까지는 **Action** 장르의 게임이 인기 있다고 볼 수 있다. 

![image](https://user-images.githubusercontent.com/99347825/202903749-4373b1ba-69e9-4c3b-ab12-cc9d489460aa.png)
### => 2000년대 이후로 가장 많이 출고된 게임 장르는 Action이기에 **다음 분기 게임 장르는 Action**으로 설계한다.

#### 2-2. 플랫폼
![image](https://user-images.githubusercontent.com/99347825/202903821-8e3658c1-8780-4d2b-a0a3-d13bb35d502b.png)
* PS3와 X360, PS2 모두 점점 **감소**하는 추세를 보인다

![image](https://user-images.githubusercontent.com/99347825/202903875-468f92ef-9009-4c04-93c8-02d9043acad6.png)
* 2012년 이후에는 **PS3, PS4, X360**의 출고량이 우세함을 알 수 있다.

![image](https://user-images.githubusercontent.com/99347825/202903938-49bee3d3-8746-4191-a275-42f6537e7e95.png)
* **PS3와 X360**은 점점 **감소**하는 추세를 보이고, **PS4**는 **증가**하는 추세를 보인다.


### => 따라서 Platform은 PS4로 설계한다.

### 3. 어떤 지역을 대상으로 게임을 설계해야 할까?
#### 네 지역 게임 출고량에 차이가 없다면 네 지역 모두를 대상으로 게임을 설계할 것이고, 만약 차이가 있다면 평균 출고량이 높은 지역을 대상으로 게임 설계할 것이다.
* 세 개 이상 집단의 차이를 검정하기 위해 **ANOVA분석** 실행
![image](https://user-images.githubusercontent.com/99347825/202904151-59501064-d9a9-4291-9c13-bc5a6c08e3a6.png)
* 네 지역을 비교했을 때, 일본을 제외하고 세 지역을 비교했을 때, 기타지역을 제외하고 세 지역을 비교했을 때 모두 적어도 한 개 이상의 지역에서 평균 출고량이 다르다고 볼 수 있다.

![image](https://user-images.githubusercontent.com/99347825/202904288-55fe0ff9-51f9-4504-9d2f-d5956f5f480c.png)
* 각 지역별 평균 그래프를 살펴봤을 때, 일본과 기타지역의 출고량은 낮고 북미지역의 평균 출고량이 가장 높다.
* 북미지역과 유럽지역의 평균 출고량을 비교하기 위한 T-test를 진행한 결과 두 지역의 평균 출고량에는 차이가 없다고 볼 수 있다.

### => 따라서 북미지역과 유럽지역을 대상으로 게임을 설계한다.

## 최종 결론
![image](https://user-images.githubusercontent.com/99347825/202904375-7717dae5-45fa-4f0c-abf0-8d1a0dbf5f9a.png)
* 모든 지역에서 높은 인기를 보이는 Action과 Sports장르 중 최근 출고량 1위를 차지하는 Action장르를 선택
* Action 플랫폼 중 상승세를 보이는 PS4를 플랫폼으로 설정
* 평균 출고량이 가장 높은 북미지역과 유럽지역을 대상으로 게임을 설계한다.


### + Action장르 게임 중 가장 출고량이 높은 게임에 대한 분석
![image](https://user-images.githubusercontent.com/99347825/202904528-d008f2ba-08bb-4570-98d3-b1d003b7cb51.png)
* Action 게임이 출고량 1위를 차지하기 시작한 2003년 이후 데이터를 살펴봤을 때, GTA 출고량이 가장 높기에 GTA 시리즈에 대해 분석

![image](https://user-images.githubusercontent.com/99347825/202904615-cfcabc1c-8188-4d6f-b474-a68888842954.png)
* 지역별 GTA출고량을 보면 **북미지역**에서 출고량이 가장 **높고**, **일본지역**에서 가장 **낮다.**

![image](https://user-images.githubusercontent.com/99347825/202904687-7d62aefd-7778-4102-ae3f-4208435b3559.png)
* 연도별로 보면 2013년에 출고량이 가장 높지만 그 외에 다른 특징은 보이지 않는다.

![image](https://user-images.githubusercontent.com/99347825/202904725-c6b2e2de-1147-4386-988e-24aca1dea10a.png)
* GTA 플랫폼 중 가장 출고량이 높은 것은 **PS4**이다.

### + 다른 지역들과 다른 양상을 보인 일본을 대상으로 게임을 설계한다면?
![image](https://user-images.githubusercontent.com/99347825/202904792-a2cd6cdc-945b-4fdf-a821-14b4f0ab041c.png)
* 일본에서의 게임 출고량 데이터만 뽑아서 분석

![image](https://user-images.githubusercontent.com/99347825/202904843-b806d8c7-df12-4047-81be-85291759705b.png)
* Role-Playing의 출고량이 가장 많음을 알 수 있다.

![image](https://user-images.githubusercontent.com/99347825/202904897-3715b788-6235-4fdd-a7ef-781a6b0f2944.png)
* 게임 장르별 출고량을 시간순으로 봤을 때 2005년을 기점으로 Action 장르의 출고량이 급격히 늘어났기에 최근 10년간 데이터를 바탕으로 다시 시각화를 진행했다.

![image](https://user-images.githubusercontent.com/99347825/202904954-de13eabd-eb75-48d1-847f-89d793cc0f14.png)
* 2012년 이후에는 **Action** 과 **Role-Playing** 출고량이 가장 많다.

![image](https://user-images.githubusercontent.com/99347825/202905020-17188013-9277-4172-a334-e61785fdb65c.png)
* Role-Playing과 Action 장르의 게임 플랫폼 모두 **3DS**의 출고량이 가장 많다


### 결론
![image](https://user-images.githubusercontent.com/99347825/202905078-1700b288-6a9f-4e33-82d7-2fe035e7951b.png)
* 최근 10년간 가장 인기있는 장르인 **Role-Playing**과 **Action**을 선택한다.
* 두 장르의 게임 모두 플랫폼은 **3DS**로 설계한다.

