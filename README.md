# 안녕하세요! 설미선입니다

**AI Product Engineer** | **RAG·Agent Workflow** | **Frontend to LLM**

> Python 기반 RAG·Tool Agent·멀티모달 Workflow를 구현하고, evaluation set·실행 로그·상태별 테스트로 결과를 확인해 왔습니다.  
> AI 코딩 도구로 구현 속도를 높이되, 문제 정의·구조 설계·테스트·오류 수정은 직접 수행합니다.

---

## 핵심 역량

### AI/LLM 전문성

~~~text
RAG 시스템 구축        ChromaDB + LangChain 기반 검색·응답 경로 설계
Agent Workflow          질문 분류 → RAG/Tool Agent 분기 → fallback 처리
캐시·비용 설계          ChromaDB 벡터 캐시 + Firestore 외부 API 캐시
평가와 개선             고정 evaluation set·반복 질문 실험·실행 로그 기반 확인
멀티모달 AI 통합        Solar + Gemini Vision으로 이미지·텍스트 생성 경로 구현
상태·안전 경계         재생성·dry-run·명시적 실행·수동 검토 상태 분리
~~~

### Frontend·서비스 구현

~~~text
웹 제품 구현           Next.js·TypeScript·FastAPI 기반 UI와 API 연결
데이터·외부 API        Firestore·ChromaDB·OpenAI·Football-Data·Naver Map 연동
배포 설정              Docker·Firebase·Cloud Run·Vercel 등 환경 구성 경험
빠른 프로토타이핑      Cursor·Claude·Codex 등 AI 코딩 도구 활용
~~~

---

## 기술 스택

**AI/ML**  
Python · FastAPI · LangChain · LangGraph · OpenAI · HuggingFace · ChromaDB · Gemini · Solar

**Frontend**  
Next.js · TypeScript · React · TailwindCSS · Zustand

**DevOps & Infrastructure**  
Firebase · GCP · AWS (S3, CloudFront) · Docker · Git · Vercel

**Automation & Data**  
Playwright · SQLite · Firestore

---

## 주요 프로젝트

### 1. 마장동딸 AI — 멀티모달 콘텐츠 생성·등록 Workflow

> **2025.06 ~ 2025.09** | 개인 프로젝트 | [GitHub](https://github.com/seolmiseon/majangdong_daughter_ai_portfolio)

사진과 운영 문맥을 바탕으로 콘텐츠를 생성하고, 금지어 검사·재생성·브라우저 등록 경계를 구현한 개인 프로젝트입니다.

**구현한 Workflow**

~~~text
사진 선택·문맥 생성
  → Gemini Vision·Solar 콘텐츠 생성
  → 금지어 검사 및 최대 3회 재생성
  → dry-run 기본 / 명시적 --post에서만 브라우저 등록 시도
  → 생성 결과·등록 결과·실패 사유 분리
~~~

**핵심 기술 구현**

- Gemini Vision과 Solar를 연결한 이미지·텍스트 생성 경로
- S3·CloudFront 기반 이미지 관리과 중복 사용 이력 기록
- FastAPI·Streamlit 기반 API와 관리 화면
- Playwright 기반 네이버 플레이스 등록 경로
- 리뷰 답글 Workflow의 1·2차 판단, 정책 검사, 애매한 사례의 수동 검토 대기 상태

**Tech Stack:** Python · FastAPI · LangGraph · Solar · Gemini Vision · AWS S3 · CloudFront · boto3 · Playwright · SQLite · Streamlit

자동 등록 코드를 구현한 경험과 장기 상용 운영 성과는 구분합니다. 일별 게시 빈도, 순위 변화, 비용 절감, 등록 성공률을 이 프로젝트의 검증된 성과로 주장하지 않습니다.

---

### 2. FSF — RAG·Tool Agent 기반 축구 분석 웹 프로토타입

> **2024.09 ~ 2025.12** | 팀 프로젝트 | [GitHub](https://github.com/seolmiseon/fsf-llm-platform)

검색만 필요한 질문과 여러 외부 데이터를 조합해야 하는 질문을 분류해, RAG와 Tool Agent의 실행 경로를 나눈 웹 프로토타입입니다.

**아키텍처**

~~~text
사용자 질문
  → 안전 필터·질문 유형 분류
  ├─ 단순 질문: RAG 기반 응답
  └─ 복합 질문: 필요한 Tool 선택
        → 외부 API 결과 조합
        → 캐시 miss·오류·결과 부족은 fallback 처리
~~~

**내부 평가와 캐시 실험**

- 47개 고정 평가 질문에서 46/47 정답(97.9%)
- 복합 질문 27/27
- 반복 질문 100건에서 캐시 적중률 90%
- 동일 실험 조건에서 평균 응답 시간 350ms → 50ms

위 수치는 프로젝트 내부 evaluation set과 캐시 실험 결과입니다. 장기 서비스 트래픽, 외부 고객 환경, 전용 트레이싱 도구 운영의 성과로 일반화하지 않습니다.

**핵심 기술 구현**

- FastAPI·Next.js·TypeScript·ChromaDB·Firestore·외부 API 연결
- LangChain 기반 Tool 선택 Agent와 RAG 응답 경로 분리
- ChromaDB 벡터 캐시와 Firestore 외부 API 캐시
- 정규식·LLM 기반 콘텐츠 필터링, 질문 분류, fallback 처리
- Docker와 GitHub Actions 기반 배포 설정

**Tech Stack:** Next.js · TypeScript · FastAPI · GPT-4o-mini · Gemini Flash · LangChain · ChromaDB · Firebase · GCP

---

### 3. 함께키즈 — RAG 기반 AI 육아 상담 해커톤 프로젝트

> **2025.07 ~ 2025.09** | 서울 우먼테크 해커톤 본선 진출 | [GitHub](https://github.com/seolmiseon/together-kids-hackathon)

육아 상담, 위치 기반 커뮤니티, 일정·RSVP 흐름을 하나의 웹 서비스로 연결한 프로젝트입니다.

**구현 범위**

- ChromaDB·BM25·RRF를 결합한 Hybrid Search 실험
- HuggingFace 감정 분석과 RAG 컨텍스트를 결합한 응답 경로
- 자연어 일정 파싱, RSVP 수집, Firebase FCM 알림
- GPS·Naver Map API 기반 근처 커뮤니티 탐색
- Next.js·FastAPI·Firebase 기반 UI·API 연결

**Hybrid Search 실험**

- 28개 문서, Ground Truth가 있는 5개 쿼리로 Vector Search와 Hybrid Search를 비교했습니다.
- 평균 검색 시간은 Vector 0.414초, Hybrid 0.421초로 거의 동일했습니다.
- 결과의 36.2%가 달라져 검색 다양성을 확인했고, Precision·Recall·MRR을 정확히 측정하기 위한 Ground Truth 기반을 남겼습니다.

작은 데이터셋에서 일부 순위가 악화된 결과도 확인했습니다. 따라서 Hybrid Search의 일반적 정확도 향상이나 실사용 성과는 주장하지 않으며, 데이터 확대와 문서 ID 정합성 개선을 후속 과제로 두었습니다.

**Tech Stack:** Next.js · TypeScript · FastAPI · GPT-4o-mini · HuggingFace · ChromaDB · LangChain · Firebase · Naver Maps API

---

### 4. Show Me The Data — AI 비즈니스 대시보드

> **2025.12 ~ 진행 중** | [GitHub](https://github.com/seolmiseon/show-me-the-data)

이메일·메시지의 날짜·시간·고객 정보를 구조화하고 일정 관리 흐름으로 연결하는 개인 대시보드 프로젝트입니다.

**구현 범위**

- 텍스트에서 날짜·시간·고객 정보를 추출하는 LangChain 기반 흐름
- 채용·예약·업무 등 사용 맥락별 분석 모드
- FullCalendar 기반 일정 확인·등록 화면
- Next.js와 FastAPI·Vercel Serverless Function 연결

**Tech Stack:** Next.js · TypeScript · FastAPI · GPT-4o-mini · LangChain · Pydantic · Vercel · FullCalendar

---

## GitHub Stats

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=seolmiseon&show_icons=true&theme=default&hide_border=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=seolmiseon&layout=compact&theme=default&hide_border=true)

---

## 교육

**AI 융합 서비스 개발 전문과정** | 새싹 강북캠퍼스 | 2025.06 ~ 2025.11  
→ LLM API, RAG 시스템, Vector Database, Docker, GCP

**프론트엔드 개발 심화과정** | 새싹 강동캠퍼스 | 2024.08 ~ 2024.11  
→ Next.js, TypeScript, React, Firebase, GraphQL

**프론트엔드 개발 부트캠프** | 코드스테이츠 | 2023.04 ~ 2023.10  
→ JavaScript, React, 웹 개발 기초

---

## RAG 시스템 구축 경험

### Hybrid Search 평가를 제품 개선으로 연결

함께키즈에서 Vector Search만 쓰던 흐름에 BM25와 RRF를 추가했습니다. 단순히 “검색 품질이 좋아졌다”고 결론 내리지 않고, 5개 Ground Truth 쿼리와 28개 문서로 속도·순위·결과 다양성을 비교했습니다.

~~~python
async def hybrid_search(query_text: str, top_k: int = 5):
    vector_results = await vector_store.similarity_search(query_text, k=top_k)
    keyword_results = bm25_index.get_top_n(query_text, n=top_k)
    return merge_and_rank(calculate_rrf_scores(vector_results, keyword_results))
~~~

검색 속도는 Vector 0.414초와 Hybrid 0.421초로 거의 같았고, 일부 쿼리에서는 순위가 악화됐습니다. 이 결과를 바탕으로 데이터셋 확대, 문서 ID 정합성, Precision·Recall·MRR 측정을 다음 검증 항목으로 정리했습니다.

---

## Contact

**Email**: budaxige@gmail.com  
**GitHub**: [@seolmiseon](https://github.com/seolmiseon)  
**Selected Repositories**: [FSF](https://github.com/seolmiseon/fsf-llm-platform) | [마장동딸 AI](https://github.com/seolmiseon/majangdong_daughter_ai_portfolio) | [함께키즈](https://github.com/seolmiseon/together-kids-hackathon)

---

### “RAG와 Agent Workflow로 실제 문제를 검증 가능한 흐름으로 만듭니다”

**Problem Definition → Small Workflow → Evaluation → Improvement**
