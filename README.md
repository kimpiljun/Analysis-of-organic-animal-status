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

<div align="Center">
  <img width="600" height="330" alt="Civil Bot Table" src="https://github.com/user-attachments/assets/18f592b3-929d-483e-8515-2927a08b102f" style="margin-right: 20px; display: inline-block; vertical-align: middle;" />
  <div style="display: inline-block; text-align: left; max-width: 500px; vertical-align: middle;">
    <h4>🧮텍스트 마이닝을 통한 동물 발견 장소적 특징 그래프</h4>
    <p>보호센터 주소 및 발견 장소를 정제하여 지리정보 기반 분석 가능하도록 가공<br>
    사람들의 유동이 많은 지역(아파티, 학교.유치원 등)에서 많이 발견되는 추세</p>
  </div>
</div>

### 2. 🔗 연관 규칙 분석

<div align="Center">
  <img width="600" height="330" alt="Civil Bot Table" src="https://github.com/user-attachments/assets/47de1a14-87c5-4a00-a34c-1651f0cc0c9d" style="margin-right: 20px; display: inline-block; vertical-align: middle;" />
  <div style="display: inline-block; text-align: left; max-width: 500px; vertical-align: middle;">
    <h4>트랜잭션을 통한 연관규칙 분석</h4>
    <p>지역별 유기동물 발견 장소 및 환경적 특성 간의 연관 규칙 도출<br>
    예: 부평 고양이 → "주차장", "아파트" / 전주 고양이 → "놀이터", "학교"</p>
  </div>
</div>

### 3. 🗺️ GIS 분석

<div align="Center">
  <img width="600" height="330" alt="Civil Bot Table" src="https://github.com/user-attachments/assets/c6fb84d6-c1e5-4639-ade3-de26abce099b" style="margin-right: 20px; display: inline-block; vertical-align: middle;" />
  <div style="display: inline-block; text-align: left; max-width: 500px; vertical-align: middle;">
    <h4>지도 시각화를 통해 유기동물 발생 밀집 지역 파악</h4>
    <p>지역별 유기동물 발견 장소 및 환경적 특성 간의 연관 규칙 도출<br>
    지도 시각화를 통해 유기동물 발생 밀집 지역 파악</p>
  </div>
</div>



### 4. 📈 시계열 분석

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
  </div>
</div>

<div align="Center">
  <img width="600" height="330" alt="Civil Bot Table"   src="https://github.com/user-attachments/assets/7cb23f3f-c00d-47ac-8410-8dd987e3c43a"  style="margin-right: 20px; display: inline-block; vertical-align: middle;" />
  <div style="display: inline-block; text-align: left; max-width: 500px; vertical-align: middle;">
    <h4>1차 차분</h4>
  </div>
</div>

<div align="Center">
  <img width="600" height="330" alt="Civil Bot Table"  src="https://github.com/user-attachments/assets/6b46a6f7-6f80-465f-b148-faa24cb0031a"   style="margin-right: 20px; display: inline-block; vertical-align: middle;" />
  <div style="display: inline-block; text-align: left; max-width: 500px; vertical-align: middle;">
    <h4>ACF 확인</h4>
  </div>
</div>

<div align="Center">
  <img width="600" height="330" alt="Civil Bot Table"  src="https://github.com/user-attachments/assets/6e436392-cbe1-4597-be90-a031540691dc"   style="margin-right: 20px; display: inline-block; vertical-align: middle;" />
  <div style="display: inline-block; text-align: left; max-width: 500px; vertical-align: middle;">
    <h4>PACF 확인</h4>
  </div>
</div>

<div align="Center">
  <img width="600" height="330" alt="Civil Bot Table"  src="https://github.com/user-attachments/assets/654357f9-fd5c-4365-80cd-c7e6f1ccdaa7"   style="margin-right: 20px; display: inline-block; vertical-align: middle;" />
  <div style="display: inline-block; text-align: left; max-width: 500px; vertical-align: middle;">
    <h4>최종 모델</h4>
  </div>
</div>

    
* 과거 데이터를 기반으로 월별 유기동물 발생 예측
* `2019.10 ~ 2021.12` 데이터 기반 `2022.09`까지의 예측 수행

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

## 🧭 향후 활용 방안

* 🎥 **CCTV/센서 설치 최적화**:

  * 빈발 지역 기반 사전 설치 및 탐지 체계 구성
* 🏢 **지자체별 대응 정책 수립**:

  * 시·군·구별 발생 특성 기반 맞춤형 대응 가능
* 🔗 **실시간 연계 시스템 구축**:

  * 데이터 표준화 후 관할 지자체·경찰서 자동 알림 체계 연계 가능

## 📘 작성자

**김필준 (Piljun Kim)**
📧 [kimpj1997@naver.com](mailto:kimpj1997@naver.com)

> *"데이터 기반의 정책이 사람과 동물이 공존하는 사회를 만듭니다."*
