# SKT-AI-Fellowship-6th
SK Telecom에서 주최하는 AI Fellowship 6기 프로젝트 연구

## Image-based Layout Generation with LLM for Advertising Poster

SKT ‘AI 디자이너’ 서비스에 적용될 포스터 자동 생성 모델의 PoC를 위한 프로젝트입니다.  
입력된 상품 이미지와 텍스트를 바탕으로 **디자인된 광고 포스터를 자동으로 생성**하는 알고리즘을 개발하였습니다.

## 프로젝트 개요

- **진행 기간**: 2024.05 ~ 2024.10 (6개월)
- **프로젝트 형태**: SKT AI Fellowship 과제 (총 3인 / 팀장)
- **도입 예정 서비스**: SKT ‘AI 디자이너’
- **주요 분야**: Automatic Poster Generation, Multimodal LLM
- **사용 기술**: PyTorch, Huggingface, Deepspeed, Codellama 7B, DINOv2, HTML Template

---

## 목표

- 입력된 **상품 이미지 + 텍스트**를 기반으로 한 광고 포스터 생성
- 텍스트 레이아웃, 색상, 배경, 키워드 강조, 이미지 크기 등을 **모델이 자동으로 결정**
- Codellama의 HTML 지식을 활용해 HTML 기반 포스터 레이아웃 생성

---

## 주요 기능

| 기능 | 설명 |
|------|------|
| HTML 기반 포스터 생성 | Codellama 7B의 HTML 사전 지식을 활용한 구조화된 레이아웃 출력 |
| 이미지 + 텍스트 멀티모달 인식 | 상품 이미지와 텍스트를 모두 고려하여 포스터 구성 |
| 구성 요소 자동 배치 | 다수의 상품군, 텍스트, 데코레이션 요소 등을 자동 생성 및 배치 |
| 한국어 텍스트 처리 | 줄바꿈, 키워드 강조, 정렬 등 디자인 요소 포함 |
| 효율적 학습 환경 | Deepspeed ZeRO-3 + PEFT를 활용한 분산 학습 |

---

## 기술 스택

- `Deepspeed`: ZeRO-3로 학습 최적화
- `PEFT`: Parameter-efficient fine-tuning
- `Python`, `PyTorch`, `Huggingface Transformers`

---

## 성과

- 기존 연구 대비 주요 평가지표 **30% 내외 개선**
- **1분 이내** 완성도 높은 포스터 자동 생성
- **특허 출원 완료**: `출원번호 10-2025-0002121`

