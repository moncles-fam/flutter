# 성동구 AI 불법현수막 탐지 MVP
## 소개
- 성동구청과 시범계약 체결할 때 제출했던 MVP입니다.
- 사용자가 촬영한 현수막의 합불법을 판단하는 앱니다.
- 합불 판단에 대한 기준은 현수막에서 추출한 텍스트를 기반으로 판단합니다.
- 옥외광고법 8조를 학습한 GPT가 현수막의 내용을 판단하여 합불 여부를 내립니다.

<a href="https://ibb.co/pnMLG9h"><img src="https://i.ibb.co/rvzwT1d/banner.png" alt="banner" border="0"></a>
## 플러터 구조
- 현재 구조는 MVP의 의도와 맞지 않게 과하게 유지보수와 확장성을 고려하였습니다.
- 이러한 구조를 채택한 이유는 큰 프로젝트에 맞는 구조를 공부하다가 마침 제의가 들어와서 적용해보았습니다.
---
- constants
  - 앱 전반적으로 재사용되는 요소들을 모아놨습니다.
- core
  - 데이터 처리, 확장성, UI 컴포넌트를 어떻게 구현할 지에 대한 세부적인 사항을 기술합니다.
- data
  - API, 로컬 저장소와 앱 사이의 다리 역할을 맡습니다. 데이터의 변경이 앱에 미치는 영향을 최소화합니다.
- domain
  - 앱의 비즈니스 로직과 엔티티를 정의합니다. 무엇을 해야하는 지에 초점이 맞추어져 있습니다.
- presentation
  - 보여지는 시각적 표현을 담당합니다.
- utils
  - 앱 전반적으로 재사용 가능한 함수와 클래스를 관리합니다. constant와 차이점은 utils는 주로 기능적인 부분을 지원합니다. constant는 변경되지 않는 데이터를 관리합니다.
## 아키텍처 구조
<a href="https://ibb.co/9T4X1bx"><img src="https://i.ibb.co/jMwKQyC/image.png" alt="image" border="0"></a>

## 플로우 차트
<a href="https://ibb.co/6rZCZrz"><img src="https://i.ibb.co/7jzmzjP/9.png" alt="9" border="0"></a>

