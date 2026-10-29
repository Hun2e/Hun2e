# 👋 안녕하세요, 임채훈입니다.

문제를 정의하고 기술로 해결하는 과정을 중요하게 생각하는 주니어 개발자입니다.  

---

## 🛠 Tech Stack

**Language** &nbsp; ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black) ![C#](https://img.shields.io/badge/C%23-239120?style=flat-square&logo=csharp&logoColor=white)

**Backend** &nbsp; ![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white) ![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)

**Frontend** &nbsp; ![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black) ![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)

**AI / Data** &nbsp; ![OpenAI](https://img.shields.io/badge/OpenAI_API-412991?style=flat-square&logo=openai&logoColor=white) ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white) ![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white) ![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black) ![Google Cloud](https://img.shields.io/badge/Google_Cloud_STT%2FTTS-4285F4?style=flat-square&logo=googlecloud&logoColor=white)

**Infra / Tools** &nbsp; ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white) ![Unity](https://img.shields.io/badge/Unity-000000?style=flat-square&logo=unity&logoColor=white) ![Notion API](https://img.shields.io/badge/Notion_API-000000?style=flat-square&logo=notion&logoColor=white)

---

## ⭐ Featured Projects

### 🗓 일정 관리 풀스택 서비스 — MyNotionAI
> 자연어 문장으로 일정 초안을 만들고 캘린더에서 관리하는 서비스 (개인 프로젝트 · 2026.02~)

| 구분 | 내용 |
|------|------|
| **역할** | 기획 → 설계 → 구현 전 과정 (1인 개발) |
| **Backend** | Spring Boot 3.2, Spring Security, JWT, JPA, Flyway, MySQL / H2 |
| **Frontend** | React 19, Vite 7, TanStack Query, Zustand |

- 자연어 입력에서 날짜·시간을 규칙 기반으로 해석해 일정 초안 생성 → 사용자가 적용/수정/취소
- JWT 인증 + Google ID 토큰 로그인, 사용자 간 데이터 격리
- 예외 경로 중심 테스트 48건(권한 경계, 위조·만료 토큰 거부, 월 경계 반개구간 조회)
- README에 알려진 문제와 단계별 로드맵(LLM 해석 + 규칙 기반 폴백 등)을 공개해 관리

👉 [github.com/Hun2e/MyNotionAI](https://github.com/Hun2e/MyNotionAI)

---

### 🧱 RAG 기반 레고 지식·제작 도우미 — REG
> 레고 스타워즈 세트를 검색·질문하고, 보유 부품으로 만들 수 있는 세트를 추천받는 챗봇 (SSAFY AI 코어 프로젝트 · 개인 · 2026.10)

| 구분 | 내용 |
|------|------|
| **역할** | PM — 설계 결정, 작업지시서 작성·검토, 평가셋 채점 (구현은 Claude Code·Codex 활용) |
| **Tech** | Python, LangGraph, ChromaDB, FastAPI, Streamlit, SQLite |

- Rebrickable 세트 메타데이터 + 위키백과 문서, 두 갈래 RAG를 LangGraph `retrieve → generate`로 결합
- 숫자(부품 수·연도·부족 수량)는 LLM이 아닌 DB 계산에서만 가져오고, 답변 후 수치 사후 검증
- MMR 검색 도입으로 Recall@5 0.65 → 0.875, 수치 정확도 1/11 → 11/11 (자체 평가셋 기준)

👉 [github.com/Hun2e/REG](https://github.com/Hun2e/REG)

---

### 🖼 이미지 기반 4지선다 VQA — AI_Challenge
> 간판·메뉴판 사진과 질문을 보고 정답을 고르는 VLM 대회 (SSAFY AI Challenge 2 · 팀 · 2026.09~10)

| 구분 | 내용 |
|------|------|
| **역할** | 개인 실험 라인(A~D, E1~E8) 설계·실행 |
| **Tech** | Python, Qwen3.5 VLM, LoRA / QLoRA, Kaggle |

- 한 번에 하나만 바꿔 비교하고, McNemar 검정을 통과하지 못하면 개선으로 기록하지 않는 실험 원칙
- OCR 추가·프롬프트 기법은 효과 없음을 확인, 모델 크기와 LoRA 학습이 실제 지렛대임을 검정으로 확인
- 개인 최고 Kaggle Public 0.97140 (팀이 만든 Order4·Zoom 추론 기법을 옮겨 적용)
- **팀 최종 성과: Kaggle Public 0.97497, 217팀 중 21위**

👉 [github.com/Hun2e/AI_Challenge](https://github.com/Hun2e/AI_Challenge)

---

### 🔍 채용공고 자동 발견·추적기 — Jasoseol-tracking
> 자소설닷컴 공고를 매일 찾아 Notion DB에 올리고, 관심 공고는 매시간 마감일·경쟁률을 갱신 (개인 · 2026.03~ 운영 중)

| 구분 | 내용 |
|------|------|
| **역할** | 설계·구현·운영 (1인) |
| **Tech** | Python, requests, BeautifulSoup, Notion API, GitHub Actions |

- SPA라 HTML 크롤링이 안 되는 목록 페이지에서 내부 목록 API를 찾아 브라우저 없이 수집
- 실제 데이터로 필터를 네 차례 고침: 제목만 검사, 영문 약어 단어 경계, IT 기업 한정 공채 구제, 교육과정 제외
- 운영 중 나온 오탐 사례를 회귀 테스트 30건으로 고정, push·PR마다 GitHub Actions에서 실행

👉 [github.com/Hun2e/Jasoseol-tracking](https://github.com/Hun2e/Jasoseol-tracking)

---

### 🧠 AI NPC 기반 VR 재난 대피 교육 시스템 — AI-NPC-VR-Safety-Training
> VR 환경에서 음성으로 상호작용하는 AI NPC 안전 교육 시스템 (팀 6인 / POSCO Academy)

| 구분 | 내용 |
|------|------|
| **담당** | AI NPC 파트 (상호작용 로직, 음성 파이프라인, 대화 시스템) |
| **Tech** | Unity, C#, OpenAI API, Google Cloud STT / TTS, Meta Quest 3 |

- **STT → LLM → TTS** 음성 파이프라인 설계 및 구현
- 화재 위치·사용자 위치 등 상황 정보를 프롬프트에 주입해 상황별 대피 안내 분기
- 음성 처리 단계 분리와 예외 처리로 실시간 응답 안정성 확보

👉 [github.com/Hun2e/AI-NPC-VR-Safety-Training](https://github.com/Hun2e/AI-NPC-VR-Safety-Training)

---

### 📊 대형마트 빅데이터 분석 — Supermarket-Analytics
> 고객 구매 데이터를 분석해 매출·이탈 개선 전략을 도출 (팀 6인 / POSCO Academy · 발표회 4팀 중 1위)

| 구분 | 내용 |
|------|------|
| **담당** | 데이터 전처리, EDA, 연관분석, 시계열 분석 |
| **Tech** | Python, pandas, Apriori, ARIMA, Random Forest |

- 결측치·이상치 처리와 파생변수 생성, 고객·시간·지점별 구매 패턴 EDA
- Apriori 연관분석으로 교차 판매 후보, ARIMA로 수요 계절성 분석
- 분석 결과를 프로모션·재고·마케팅 전략으로 연결

👉 [github.com/Hun2e/Supermarket-Analytics](https://github.com/Hun2e/Supermarket-Analytics)

---

## 📚 Learning & Growth

### ⚛️ React 학습 정리 — Studying-React
> 인프런 「한 입 크기로 잘라먹는 리액트」 강의 실습 코드 정리 (2025.12 ~ 진행중 · 60%)  
> 컴포넌트 설계, useState, useEffect, useRef, useMemo 등 핵심 Hook 학습

👉 [github.com/Hun2e/Studying-React](https://github.com/Hun2e/Studying-React)

### 🌱 Spring Boot 학습 정리 — Studying_Spring
> 인프런 「스프링 입문 - 코드로 배우는 스프링 부트, 웹 MVC, DB 접근 기술」 (2026.01 ~ 진행중)  
> Spring Boot 기본 구조, 웹 MVC, JPA 실습 기록

👉 [github.com/Hun2e/Studying_Spring](https://github.com/Hun2e/Studying_Spring)

---

## ✉️ Contact

📧 [cogns3824@naver.com](mailto:cogns3824@naver.com)
