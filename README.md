# 🐾 유기동물 발생 요인 분석 프로젝트

> "유기동물은 갑자기 생기지 않습니다. 우리는 데이터를 통해 그 원인을 추적합니다."

---

## 🎯 프로젝트 개요

최근 몇 년간 유기동물의 수가 꾸준히 증가하고 있으며, 이로 인한 민원도 급증하고 있습니다. 유기동물의 수 증가에 따라 안락사도 늘어나고 있지만, 명확한 예방 및 사후처리 방법은 부재한 실정입니다. 이에 따라 본 프로젝트는 유기동물의 발생 특성을 파악하고, 효과적인 예방 및 대응 방안을 제안하고자 기획되었습니다.

---

## 📂 데이터 및 도구

* **데이터 출처**: 2019년 \~ 2022년 유기동물 데이터
* **분석 도구**:

  * ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge\&logo=python\&logoColor=white)
  * ![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge\&logo=R\&logoColor=white)
* **역할 분담**:

  * **Python**: 전처리, 텍스트 마이닝 중심
  * **R**: 통계 분석, 연관 규칙, 시계열 예측 등
* **주요 변수**: `HAPPENDT`, `HAPPENPLACE`, `KIND`, `SEXCD`, `AGE`, `PROCESSSTATE`, `CAREADDR` 등

---

## 🧪 분석 방법론

### 1. 📌 텍스트 마이닝

> 유기동물 데이터 내 보호센터 주소 및 발견 장소와 같은 비정형 텍스트 데이터를 정제하고 가공하여 분석에 활용하였습니다. 텍스트 마이닝 기법을 통해 장소명, 시설명 등 핵심 키워드를 추출하고, 이를 기반으로 유기동물이 주로 발견되는 장소적 특성을 파악할 수 있었습니다.

> 특히, 사람이 많이 모이는 아파트 단지, 학교, 유치원 등 특정 지역에서 유기동물 발견 빈도가 높게 나타나는 경향을 확인하였습니다. 이를 통해 유기동물 발생과 지역사회 환경 간의 연관성을 탐색하는 기초 자료를 마련하였습니다.

<div align="Center">
  <img width="600" height="330" alt="Civil Bot Table" src="https://github.com/user-attachments/assets/18f592b3-929d-483e-8515-2927a08b102f" style="margin-right: 20px; display: inline-block; vertical-align: middle;" />
  <div style="display: inline-block; text-align: left; max-width: 500px; vertical-align: middle;">
    <h4>🧮텍스트 마이닝을 통한 동물 발견 장소적 특징 그래프</h4>
    <p>보호센터 주소 및 발견 장소를 정제하여 지리정보 기반 분석 가능하도록 가공<br>
    사람들의 유동이 많은 지역(아파티, 학교.유치원 등)에서 많이 발견되는 추세</p>
  </div>
</div>

### 2. 🔗 연관 규칙 분석

> 유기동물 발견 장소와 주변 환경 특성 간의 연관성을 규칙 기반으로 도출하기 위해 연관 규칙 분석을 수행하였습니다. 트랜잭션 형태로 정리된 데이터를 바탕으로 지역별로 자주 함께 나타나는 장소 조합을 찾아내었으며, 예를 들어 부평 지역의 고양이는 주차장과 아파트 주변에서, 전주 지역의 고양이는 놀이터와 학교 인근에서 주로 발견되는 패턴을 확인하였습니다.

> 이 분석은 유기동물 발생과 특정 환경 요인 간의 상호작용을 이해하고, 지역 맞춤형 예방 대책 수립에 중요한 인사이트를 제공합니다.
<div align="Center">
  <img width="600" height="330" alt="Civil Bot Table" src="https://github.com/user-attachments/assets/47de1a14-87c5-4a00-a34c-1651f0cc0c9d" style="margin-right: 20px; display: inline-block; vertical-align: middle;" />
  <div style="display: inline-block; text-align: left; max-width: 500px; vertical-align: middle;">
    <h4>트랜잭션을 통한 연관규칙 분석</h4>
    <p>지역별 유기동물 발견 장소 및 환경적 특성 간의 연관 규칙 도출<br>
    예: 부평 고양이 → "주차장", "아파트" / 전주 고양이 → "놀이터", "학교"</p>
  </div>
</div>

### 3. 🗺️ GIS 분석

> 유기동물 발생 데이터를 지리정보시스템(GIS) 기법으로 시각화하여 전국 및 지역별 발생 밀집도를 파악하였습니다. 행정구역 단위로 발생 건수를 색상으로 표현함으로써 유기동물이 집중적으로 발생하는 지역을 한눈에 확인할 수 있었으며, 이를 통해 특정 지역의 환경적 특성이나 인구 밀집도와의 상관관계를 탐색할 수 있었습니다.

> GIS 분석은 공간적 패턴을 명확히 하여 정책 결정자들이 효율적인 자원 배분과 예방 활동을 계획하는 데 중요한 근거 자료로 활용됩니다.
<div align="Center">
  <img width="600" height="330" alt="Civil Bot Table" src="https://github.com/user-attachments/assets/c6fb84d6-c1e5-4639-ade3-de26abce099b" style="margin-right: 20px; display: inline-block; vertical-align: middle;" />
  <div style="display: inline-block; text-align: left; max-width: 500px; vertical-align: middle;">
    <h4>지도 시각화를 통해 유기동물 발생 밀집 지역 파악</h4>
    <p>지역별 유기동물 발견 장소 및 환경적 특성 간의 연관 규칙 도출<br>
    지도 시각화를 통해 유기동물 발생 밀집 지역 파악</p>
  </div>
</div>



### 4. 📈 시계열 분석

> 유기동물 발생 데이터의 시간적 변화를 분석하기 위해 시계열 분석을 수행하였습니다. 먼저, 원시 데이터(tsData)를 시각화하여 전체적인 추세와 변동성을 확인하였고, ACF(자기상관함수) 그래프를 통해 시계열 내에서 시차(lag)에 따른 상관관계를 파악하였습니다. ACF 결과는 데이터에 계절성 및 자기상관성이 존재함을 시사합니다.

>이를 보완하기 위해 계절성 요인을 분해하여 제거하였으며, 1차 차분을 적용하여 시계열의 정상성(stationarity)을 확보하였습니다. 정상성 확보는 예측 모델링의 기본 전제 조건으로, 차분 후 시계열은 평균과 분산이 일정한 상태로 변환되어 안정적인 분석이 가능해졌습니다.

>또한, PACF(부분자기상관함수) 분석을 통해 시계열 내에서 직접적인 자기상관 구조를 확인하였고, 이를 바탕으로 최종 ARIMA 모델을 구축하였습니다. 이 모델은 유기동물 발생의 계절적 패턴과 추세를 효과적으로 반영하여 향후 발생량 예측에 활용할 수 있습니다.




<div align="Center">
  <img width="600" height="330" alt="Civil Bot Table" src="https://github.com/user-attachments/assets/19aeafbd-7387-4512-b800-ee5417913518"  style="margin-right: 20px; display: inline-block; vertical-align: middle;" />
  <div style="display: inline-block; text-align: left; max-width: 500px; vertical-align: middle;">
    <h4>데이터 분해</h4>
   <p>시계열 데이터를 추세(Trend), 계절성(Seasonality), 불규칙성(Random)으로 분해하여 각 구성 요소를 파악합니다.<br>
   이를 통해 데이터 내에 계절적 패턴이 존재하는지 확인합니다.</p>
  </div>
</div>

<div align="Center">
  <img width="600" height="330" alt="Civil Bot Table"  src="https://github.com/user-attachments/assets/9f7dcbb0-1d36-4228-b677-cf5e2f9637b9"  style="margin-right: 20px; display: inline-block; vertical-align: middle;" />
  <div style="display: inline-block; text-align: left; max-width: 500px; vertical-align: middle;">
    <h4>계절성 제거</h4>
   <p>분해 결과를 바탕으로 계절성 요인을 제거하여 비계절성 데이터로 변환합니다.<br>
   계절성에 의한 변동을 제거해 추세와 불규칙 요인에 집중할 수 있습니다.</p>
  </div>
</div>

<div align="Center">
  <img width="600" height="330" alt="Civil Bot Table"   src="https://github.com/user-attachments/assets/7cb23f3f-c00d-47ac-8410-8dd987e3c43a"  style="margin-right: 20px; display: inline-block; vertical-align: middle;" />
  <div style="display: inline-block; text-align: left; max-width: 500px; vertical-align: middle;">
    <h4>1차 차분</h4>
   <p>정상성 확보를 위해 시계열에 차분을 적용합니다.<br>
   차분 후 데이터가 평균과 분산이 일정한 정상 시계열로 변환되었는지 확인합니다.</p>
  </div>
</div>

<div align="Center">
  <img width="600" height="330" alt="Civil Bot Table"  src="https://github.com/user-attachments/assets/6b46a6f7-6f80-465f-b148-faa24cb0031a"   style="margin-right: 20px; display: inline-block; vertical-align: middle;" />
  <div style="display: inline-block; text-align: left; max-width: 500px; vertical-align: middle;">
    <h4>ACF 확인</h4>
   <p>차분된 시계열의 자기상관함수를 확인하여 시계열 내의 상관 구조를 파악합니다.<br>
   모델 차수 결정에 참고합니다.</p>
  </div>
</div>

<div align="Center">
  <img width="600" height="330" alt="Civil Bot Table"  src="https://github.com/user-attachments/assets/6e436392-cbe1-4597-be90-a031540691dc"   style="margin-right: 20px; display: inline-block; vertical-align: middle;" />
  <div style="display: inline-block; text-align: left; max-width: 500px; vertical-align: middle;">
    <h4>PACF 확인</h4>
   <p>부분 자기상관함수를 통해 직접적인 자기상관 관계를 분석합니다.<br>
   AR(자기회귀) 모형 차수 결정에 활용됩니다.</p>
  </div>
</div>

<div align="Center">
  <img width="600" height="330" alt="Civil Bot Table"  src="https://github.com/user-attachments/assets/654357f9-fd5c-4365-80cd-c7e6f1ccdaa7"   style="margin-right: 20px; display: inline-block; vertical-align: middle;" />
  <div style="display: inline-block; text-align: left; max-width: 500px; vertical-align: middle;">
    <h4>최종 모델</h4>
   <p>위 분석을 토대로 ARIMA 등 적절한 시계열 모델을 구축하고, 예측 및 해석을 수행합니다.</p>
  </div>
</div>

---

## 🔍 주요 분석 결과

* 🐶 **12%의 높은 반환률** → 입양자 대상의 유기 예방 교육 필요
* 🐕 **품종별 반환률 차이**:

  * 리트리버, 시바, 허스키 순으로 반환률 높음
  * 품종 기반 보호 기간 차등 적용 가능
* 📊 **지역별 분포 특성**:

  * 경기·경남·제주 유기견·유기묘 다수
  * 전라·부산·강원은 인구 대비 비율 높음
* 🏠 **발견 장소 규칙성**:

  * 고양이 → 주차장, 아파트 / 놀이터, 학교
  * 개 → 길가, 공터 등 상대적으로 무작위성 존재

---

## 🧭 향후 활용 방안

* 🎥 **CCTV/센서 설치 최적화**:

  * 빈발 지역 기반 사전 설치 및 탐지 체계 구성
* 🏢 **지자체별 대응 정책 수립**:

  * 시·군·구별 발생 특성 기반 맞춤형 대응 가능
* 🔗 **실시간 연계 시스템 구축**:

  * 데이터 표준화 후 관할 지자체·경찰서 자동 알림 체계 연계 가능

---

## 🧑‍💻 작성자

**김필준 (Piljun Kim)**
📧 [kimpj1997@naver.com](mailto:kimpj1997@naver.com)
🔗 [Notion 포트폴리오 보기](https://www.notion.so/238481d8bb1080f2a68feea0d4459014)

> *"데이터 기반의 정책이 사람과 동물이 공존하는 사회를 만듭니다."*
