# 👋 안녕하세요, 임채훈입니다.

문제를 정의하고 기술로 해결하는 과정을 중요하게 생각하는 주니어 개발자입니다.  

---

## 🛠 Tech Stack

**Language** &nbsp; ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black) ![C#](https://img.shields.io/badge/C%23-239120?style=flat-square&logo=csharp&logoColor=white)

**Backend** &nbsp; ![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white) ![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)

**Frontend** &nbsp; ![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black) ![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)

**AI / Data** &nbsp; ![OpenAI](https://img.shields.io/badge/OpenAI_API-412991?style=flat-square&logo=openai&logoColor=white) ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white) ![Google Cloud](https://img.shields.io/badge/Google_Cloud_STT%2FTTS-4285F4?style=flat-square&logo=googlecloud&logoColor=white)

**Infra / Tools** &nbsp; ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white) ![Unity](https://img.shields.io/badge/Unity-000000?style=flat-square&logo=unity&logoColor=white) ![Notion API](https://img.shields.io/badge/Notion_API-000000?style=flat-square&logo=notion&logoColor=white)

---

## ⭐ Featured Projects

### 🗓 AI 기반 일정 관리 서비스 — MyNotionAI
> AI와의 대화로 일정을 등록·수정·요약하는 풀스택 캘린더 서비스 (개인 프로젝트)

| 구분 | 내용 |
|------|------|
| **역할** | 서비스 기획 → 설계 → 구현 전 과정 (1인 개발) |
| **Frontend** | React 19, Vite 7, TanStack Query, Zustand, React Router 7 |
| **Backend** | Spring Boot 3.2, Spring Security, JWT, JPA, MySQL / H2 |
| **AI** | OpenAI API 기반 일정 분석·수정·요약, Google OAuth 로그인 |

- 자연어 입력 → AI가 날짜·시간 해석 후 일정 초안 생성 및 적용
- JWT 인증 + Google OAuth 토큰 로그인 지원
- 월별 캘린더 UI에서 일정 CRUD 및 AI 대화 로그 조회
- 동작하는 MVP 완성 후 LLM 보조 해석·테스트 코드 등 품질 개선 진행 중

👉 [github.com/Hun2e/MyNotionAI](https://github.com/Hun2e/MyNotionAI)

---

### 🔍 채용공고 자동 트래커 — Recruitment-notice-Tracking
> 관심 채용공고를 자동 수집해 Notion DB에서 D-day까지 한눈에 관리하는 자동화 시스템

| 구분 | 내용 |
|------|------|
| **역할** | 전체 설계 및 구현 (1인) |
| **Tech** | Python, BeautifulSoup, Notion API, GitHub Actions |

- `cron: "0 * * * *"` — 서버 없이 매시간 GitHub Actions로 자동 실행
- 자소설닷컴 크롤링 → 회사명·마감일·직무별 작성자 수 자동 추출
- Notion API upsert로 신규 등록 / 업데이트 자동화
- D-day 자동 계산: `진행중` / `D-3` / `D-1` / `오늘 마감` / `마감됨`
- GitHub Secrets로 API 키 등 민감 정보 보안 관리

<details>
<summary>🔧 고도화 계획 — Spring + React 풀스택으로 전환 예정</summary>

| 구분 | 현재 (v1) | 목표 (v2) |
|------|-----------|-----------|
| **크롤링** | Python 스크립트 | Spring Batch / Scheduler |
| **데이터 저장** | Notion API | MySQL + Spring Data JPA |
| **실행 방식** | GitHub Actions cron | Spring 내장 스케줄러 |
| **UI** | Notion 페이지 | React 기반 대시보드 |

- 공고 현황을 Notion 대신 **직접 만든 웹 UI**에서 확인
- 다양한 채용 사이트로 크롤링 소스 확장 가능한 구조로 설계 예정

</details>

👉 [github.com/Hun2e/Recruitment-notice-Tracking](https://github.com/Hun2e/Recruitment-notice-Tracking)

---

### 🧠 AI NPC 기반 VR 재난 대피 교육 시스템 — AI-NPC-VR-Safety-Training
> VR 환경에서 음성으로 상호작용하는 AI NPC를 구현한 실감형 안전 교육 시스템 (팀 프로젝트 6인 / POSCO Academy)

| 구분 | 내용 |
|------|------|
| **담당** | AI NPC 파트 전담 (상호작용 로직, 음성 파이프라인, 대화 시스템) |
| **Tech** | Unity, C#, OpenAI API, Google Cloud STT / TTS, Meta Quest 3 |

- **STT → LLM → TTS** 음성 파이프라인 설계 및 구현
- 화재 위치·사용자 위치 등 재난 상황 정보를 프롬프트에 주입 → 상황 기반 대피 안내 분기 처리
- 일반 LLM의 맥락 부족 문제 → Prompt Engineering으로 응답 정확도 개선
- 음성 처리 파이프라인 분리 및 예외 처리로 실시간 응답 안정성 확보
- 기존 일방향 VR 안전 교육을 **양방향 대화형 교육**으로 전환

👉 [github.com/Hun2e/AI-NPC-VR-Safety-Training](https://github.com/Hun2e/AI-NPC-VR-Safety-Training)

---

### 📊 대형마트 빅데이터 분석 프로젝트 — Supermarket-Analytics
> 고객 구매 데이터를 분석해 매출 증대 및 고객 이탈 개선 전략을 도출한 데이터 분석 프로젝트 (팀 프로젝트 6인 / POSCO Academy)

| 구분 | 내용 |
|------|------|
| **담당** | 데이터 전처리, EDA, 연관분석, 시계열 분석 파트 |
| **Tech** | Python, pandas, numpy, Apriori, ARIMA, Random Forest, matplotlib, seaborn |

- 고객·상품·거래 데이터 전처리 (결측치·이상치 제거 및 파생변수 생성)
- EDA를 통한 고객별·시간별·지점별 구매 패턴 분석
- **연관분석(Apriori)** 으로 상품 묶음 및 교차 판매 가능성 도출
- **시계열 분석(ARIMA)** 으로 주요 상품 수요 변동 및 계절성 예측
- **Random Forest** 기반 이탈 가능 고객 사전 식별 근거 확보
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

## 📈 GitHub Stats

[![GitHub Stats](https://github-readme-stats.vercel.app/api?username=Hun2e&show_icons=true&hide_border=true&bg_color=00000000&title_color=58a6ff&text_color=c9d1d9&icon_color=58a6ff)](https://github.com/Hun2e)

---

## ✉️ Contact

📧 [cogns3824@naver.com](mailto:cogns3824@naver.com)
