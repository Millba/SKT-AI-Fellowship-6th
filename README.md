# SKT-AI-Fellowship-6th
Image-based Layout Generation with LLM for Advertising Poster

# LLM 기반 광고 이미지 레이아웃 디자인 자동화

SKT ‘AI 디자이너’ 서비스에 적용될 포스터 자동 생성 모델의 PoC를 위한 프로젝트입니다.  
입력된 상품 이미지와 텍스트를 바탕으로 **디자인된 광고 포스터를 자동으로 생성**하는 알고리즘을 개발하였습니다.

## 🚀 프로젝트 개요

- **진행 기간**: 2024.05 ~ 2024.10 (6개월)
- **프로젝트 형태**: SKT AI Fellowship 과제 (총 3인 / 팀장)
- **도입 예정 서비스**: SKT ‘AI 디자이너’
- **주요 분야**: Automatic Poster Generation, Multimodal LLM
- **사용 기술**: PyTorch, Huggingface, Deepspeed, Codellama 7B, DINOv2, HTML Template

---

## 🎯 목표

- 입력된 **상품 이미지 + 텍스트**를 기반으로 한 광고 포스터 생성
- 텍스트 레이아웃, 색상, 배경, 키워드 강조, 이미지 크기 등을 **모델이 자동으로 결정**
- Codellama의 HTML 지식을 활용해 HTML 기반 포스터 레이아웃 생성

---

## 🧩 주요 기능

| 기능 | 설명 |
|------|------|
| HTML 기반 포스터 생성 | Codellama 7B의 HTML 사전 지식을 활용한 구조화된 레이아웃 출력 |
| 이미지 + 텍스트 멀티모달 인식 | 상품 이미지와 텍스트를 모두 고려하여 포스터 구성 |
| 구성 요소 자동 배치 | 다수의 상품군, 텍스트, 데코레이션 요소 등을 자동 생성 및 배치 |
| 한국어 텍스트 처리 | 줄바꿈, 키워드 강조, 정렬 등 디자인 요소 포함 |
| 효율적 학습 환경 | Deepspeed ZeRO-3 + PEFT를 활용한 분산 학습 |

---

## 기술 스택

- `Codellama 7B`: 텍스트-기반 HTML 구조 생성
- `DINOv2`: 이미지 feature 추출
- `Deepspeed`: ZeRO-3로 학습 최적화
- `PEFT`: Parameter-efficient fine-tuning
- `HTML`: 출력 포맷
- `Python`, `PyTorch`, `Huggingface Transformers`

---

## 트러블슈팅

### 요소 누락 및 겹침
- **문제**: 많은 요소 배치 시 일부 누락 또는 겹침 발생
- **해결**:
  - 입력 요소 / 생성 요소를 분리하는 **2-stage 모델 구조**
  - 겹침 현상 **100% → 35%**로 감소

### 이미지 비율 반영 문제
- **문제**: 입력 비율이 출력에 반영되지 않음
- **해결**:
  - **Chain-of-Thought (CoT)** prompting을 통해 비율 계산
  - 정상 반영 비율 **10% → 90%**로 증가

---

## 성과

- 기존 연구 대비 주요 평가지표 **30% 내외 개선**
- **1분 이내** 완성도 높은 포스터 자동 생성
- **특허 출원 완료**: `출원번호 10-2025-0002121`

