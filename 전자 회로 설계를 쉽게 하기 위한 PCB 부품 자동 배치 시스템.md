# 전자 회로 설계를 쉽게 하기 위한 PCB 부품 자동 배치 시스템
### [논문 2024](https://github.com/jcshim/AutoLayout/blob/main/Automated%20PCB%20Component%20Placement%20System%20for%20Effic.pdf)

---

### 📌 연구 목적  
- **전자 회로 설계 초보자**도 고품질 PCB를 쉽게 설계할 수 있도록 자동 배치 시스템을 개발함.
- 특히 **센서, 모터 등 주요 부품**은 LLM(대형 언어 모델),  
  **저항, 콘덴서 등 보조 부품**은 RL(강화학습)을 사용해 자동 배치.

---

### 🔧 시스템 구성

1. **입력**: 회로도 + 빈 PCB
2. **출력**: 모든 부품이 배치된 PCB

---

### 🧠 주요 기술

#### 1. LLM 기반 주요 부품 배치  
- 주요 부품(IC, 센서, 모터 등)은 기능에 맞게 LLM이 배치 전략 생성  
- 예시: RC카 모양에 따라 모터 위치 자동 배치

#### 2. RL 기반 보조 부품 배치  
- 보조 부품(저항, 콘덴서 등)은 전기적 효율 고려  
- 보드 상태 + 부품 정보를 상태(State)로, 위치 + 회전을 행동(Action)으로 결정  
- 보상(Reward):  
  - Net 길이 최소화  
  - Via 수 줄이기  
  - 논리적으로 가까운 부품 근접 배치  

---

### 🧪 구현 및 성능

- **Matrix 형태의 보드 정보**를 CNN에 입력해 RL 수행  
- 예시로 **음성 인식 조명 스위치 회로** 배치 결과,  
  라우팅 성공률 100%, 실제 사용자 스타일과 유사한 배치 달성

---

### ✅ 결론

- **주요 부품은 LLM**, **보조 부품은 RL**로 효율적인 자동 배치 구현
- **비전문가도 고품질 PCB 설계** 가능하게 함

---

필요하시면 그림이나 알고리즘 구조, 보상 함수 구성도 시각적으로 정리해드릴 수 있어요!
