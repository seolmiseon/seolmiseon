# 안녕하세요! 설미선입니다

**AI 응용 전문 개발자** | **RAG 시스템 구축 경험** | **Frontend to LLM**

> RAG + LLM 파이프라인으로 응답 속도 7배 향상, API 비용 40% 절감을 달성한 풀스택 개발자입니다.  
> Next.js/TypeScript로 사용자 친화적 UI를 구현하고, ChromaDB 기반 RAG 시스템으로 실사용자 서비스를 운영한 경험이 있습니다.

---

## 핵심 역량

### AI/LLM 전문성
```
RAG 시스템 구축        ChromaDB + LangChain → 검색 속도 0.3초
응답 속도 최적화       3단계 캐싱 전략 → 7배 향상 (350ms → 50ms)
비용 최적화           GPT-4 → GPT-4o-mini 전환 → 90% 절감
프롬프트 엔지니어링    동적 프롬프트 시스템 → 응답 품질 30% 향상
멀티모달 AI 통합      Solar + Gemini Vision 결합 → 텍스트+이미지 자동 생성
LangGraph 워크플로우   2단계 리뷰 판단 시스템 → API 호출 최소화
```

### Frontend 개발
```
실사용자 배포         Next.js/TypeScript → 6가구 운영
해커톤 본선 진출      서울 우먼테크 (38개팀 중 선발)
성능 최적화          빌드 시간 38% 단축, 로딩 2배 향상
반응형 UI            Mobile/Desktop 최적화
```

### 빠른 실행력
```
9주 완성             0→1 프로덕트 (기획-개발-배포 전체)
2주 MVP 개발         Cursor + Claude 활용한 빠른 프로토타이핑
비용 최적화          월 운영 비용 33원으로 24시간 자동화 시스템 구축
실시간 피드백 반영    6가구 운영으로 UX 개선
```

---

## 기술 스택

**AI/ML**  
Python FastAPI LangChain LangGraph OpenAI HuggingFace ChromaDB Gemini Solar

**Frontend**  
Next.js TypeScript React TailwindCSS Zustand

**DevOps & Infrastructure**  
Firebase GCP AWS (EC2, S3, CloudFront) Docker Git Vercel

**Automation & Data**  
Playwright Cron SQLite Firestore

---

## 주요 프로젝트

### 1. 마장동딸 AI - AI 기반 마케팅 자동화 플랫폼

> **2025.01 ~ 진행 중** | 포트폴리오 프로젝트 | [GitHub](https://github.com/seolmiseon/majangdong_daughter_ai_portfolio)

**소상공인을 위한 24시간 AI 마케팅 자동화 플랫폼**

광고 대행사 비용의 1/10 가격으로 AI가 24시간 자동으로 네이버 플레이스 마케팅을 수행합니다.

**정량적 성과**

- 월 운영 비용: **약 33원** (AWS S3: 3원, CloudFront: 13원, Gemini API: 17원)
- 기존 광고 대행사 대비: **99.9% 비용 절감**
- 게시 빈도: **주 14회** (1일 2회, 기존 대비 5-7배 증가)
- 처리 시간: **15-30초/게시**
- 콘텐츠 생성 성공률: **95%+** (금지어 재생성 포함)

**핵심 기술 구현**

```
멀티모달 AI 활용
    Solar Pro (텍스트 생성)
    +
    Gemini 2.0 Flash (이미지 분석)
    ↓
SEO 최적화 콘텐츠 생성 (키워드 100% 포함)

LangGraph 워크플로우
    2단계 리뷰 판단 (1차 → 애매한 경우 2차 검토)
    +
    정책 검증 루프 (최대 3회 재생성)
    ↓
악성 리뷰 자동 신고 + 맞춤 답글 생성

AWS 인프라
    S3 (이미지 저장, 중복 방지 알고리즘)
    +
    CloudFront CDN (빠른 전송, SEO 최적화)
    +
    boto3 비동기 처리
    ↓
안전하고 효율적인 이미지 관리
```

**Tech Stack:** Python FastAPI LangGraph Solar Gemini-Vision AWS-EC2 AWS-S3 CloudFront boto3 Playwright ChromaDB SQLite Streamlit

---

### 2. FSF - AI 축구 분석 플랫폼

> **2025.10 ~ 진행 중** | [Live Demo](https://fsfproject-fd2e6.web.app) | [GitHub](https://github.com/seolmiseon/fsf-llm-platform)

**RAG + LLM으로 축구 경기를 분석하는 AI 플랫폼**

**최적화 성과**

- 응답 속도 **7배 향상**: 350ms → 50ms (2단계 캐싱)
- API 비용 **40% 절감**: $1/월 → $0.60/월
- 캐시 히트율: **90%** (유사 질문 중복 제거)
- 5개 LLM API 완성: 챗봇, 경기 분석/예측, 선수 비교

**아키텍처**

```
Frontend (Next.js) → Backend (FastAPI) → LLM Service
                                            ↓
                                    OpenAI + RAG
                                            ↓
                              ChromaDB (Vector Search)
                                            ↓
                              Football-Data API
```

**하이브리드 질문 분류 시스템**

```
정규식 기반 빠른 판단 (비용 $0)
    ↓
단순 질문 → chat.py (1회 호출)
복잡 질문 → Agent (2회 호출, 자동 Tool 선택)
    ↓
정확도: 97.9% (46/47)
```

**AI Agent 시스템**

- LangChain 기반 자동 Tool 선택
- 6개 Tool: rag_search, match_analysis, player_compare, posts_search, fan_preference, calendar
- 단순 질문은 chat.py (1회 호출), 복잡 질문만 Agent (2회 호출)로 자동 분기

**콘텐츠 안전**

- 정규식 + LLM 기반 유해 콘텐츠 필터링
- 입력 게이트웨이 + 출력 필터 (욕설/스팸 자동 차단)
- LLM 기반 게시글 카테고리 자동 분류 (6개 카테고리)

**Tech Stack:** Next.js TypeScript FastAPI GPT-4o-mini Gemini-Flash LangChain ChromaDB Firebase GCP-Cloud-Run

---

### 3. 함께키즈 - RAG 기반 AI 육아 상담 플랫폼

> **2025.07 ~ 2025.09** | 해커톤 본선 진출 | [Live Demo](https://togatherkids.web.app) | [GitHub](https://github.com/seolmiseon/hackathon)

**RAG + 감정 분석 기반 24시간 AI 육아 상담 플랫폼**

**정량적 성과**

- 서울 우먼테크 해커톤 **본선 진출** (38개팀 중 선발)
- **6가구 실사용** 배포 및 운영
- 검색 속도 **0.3초** (Hybrid Search: Vector + BM25 + RRF)
- 정확도 **85% 향상** (RAG vs 하드코딩)
- API 비용 **90% 절감** (GPT-4 → GPT-4o-mini)
- 빌드 시간 **38% 단축** (292→180초)
- 감정 분석 정확도 **87%** (HuggingFace Transformers)

**핵심 기술 구현**

```
HuggingFace 감정 분석
    j-hartmann/emotion-english-distilroberta-base
    ↓
스트레스 레벨 1-5단계 자동 분류 (정확도 87%)
    ↓
감정 기반 동적 프롬프트 선택 → 응답 품질 30% 향상

Hybrid RAG 검색
    Vector Search (의미 유사도)
    +
    BM25 Keyword Search (정확한 키워드)
    +
    RRF (Reciprocal Rank Fusion) 통합
    ↓
검색 속도 0.3초, 정확도 향상

위치 기반 매칭
    GPS Geolocation + 네이버 지도 API
    ↓
도보 15분 이내 이웃 자동 연결
    ↓
공동구매/일정 공유/커뮤니티 매칭
```

**AI 기반 일정 파싱**

- 자연어에서 시간/장소/활동 자동 추출
- RSVP 필요 여부 자동 감지
- Firebase FCM 푸시 알림 통합
- 그룹 멤버 자동 조회 및 알림 전송

**Tech Stack:** Next.js TypeScript FastAPI GPT-4o-mini HuggingFace ChromaDB LangChain Firebase Naver-Maps-API

---

### 4. Show Me The Data - AI 비즈니스 대시보드

> **2025.12 ~ 진행 중** | [Live Demo](https://show-me-the-data.vercel.app) | [GitHub](https://github.com/seolmiseon/show-me-the-data)

**이메일/메시지 분석 및 일정 관리 대시보드**

**주요 기능**

- 텍스트에서 날짜/시간 자동 추출 (LangChain ExtractionChain)
- 고객/클라이언트 이름 자동 파싱
- 모드별 맞춤 분석 (채용/예약/업무)
- FullCalendar 기반 일정 자동 등록

**Full Stack Serverless**

- 프론트엔드 + 백엔드 모두 Vercel Serverless Functions로 배포
- FastAPI → Mangum → Vercel Python Runtime
- 별도 서버 불필요, Git push 시 자동 배포

**Tech Stack:** Next.js TypeScript FastAPI GPT-4o-mini LangChain Pydantic Vercel FullCalendar

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

### ChromaDB + LangChain 파이프라인

```python
# 실제 함께키즈 프로젝트 코드 패턴
async def process_rag_query(message: str):
    # 1. Embedding
    embedding = await openai.embeddings.create(
        model="text-embedding-3-small",
        input=message
    )
    
    # 2. Vector Search
    results = chroma_collection.query(
        query_embeddings=[embedding.data[0].embedding],
        n_results=5
    )
    
    # 3. Context + Prompt
    context = "\n".join(results['documents'][0])
    prompt = f"참고 정보:\n{context}\n\n질문: {message}"
    
    # 4. LLM Generation
    response = await openai.chat.completions.create(
        model="gpt-4o-mini",
        messages=[{"role": "user", "content": prompt}]
    )
    
    return response.choices[0].message.content
```

**성능 지표**

- 검색 속도: 0.3초
- 캐시 히트율: 90% (유사 질문)
- 정확도: 85% 향상 (하드코딩 대비)

---

## Contact

**Email**: budaxige@gmail.com  
**GitHub**: [@seolmiseon](https://github.com/seolmiseon)  
**Portfolio**: [함께키즈](https://togatherkids.web.app) | [FSF](https://fsfproject-fd2e6.web.app) | [Show Me The Data](https://show-me-the-data.vercel.app)

---

### "RAG와 LLM으로 실제 문제를 해결합니다"

**Real Problems → AI Solutions → User Value**
