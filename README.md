

## 기술 스택

- **언어:** `Javascript` `Typescript` `HTML` `CSS`
- **프레임워크/라이브러리:** `React` `Next.js` `jQuery`
- **빌드 도구:** `Webpack` `Vite`
- **버전 관리/협업:** `Git` `GitHub` `Slack` `Notion`
- **UI/스타일링:** `Bootstrap` `styled-components`
- **상태 관리:** `Context API` `Redux-toolkit` `Zustand`

## 자격증

- 정보처리기사
- 웹디자인기능사
- 컴퓨터활용능력 1급
- GTQ 1급

## 학력 및 경력

| 기간              | 내용                                       |
| ----------------- | ------------------------------------------ |
| 2017.03 - 2022.02 | 전남대학교 철학과 / 생활복지학과 졸업      |
| 2022.06 - 2022.12 | 그린컴퓨터아카데미 UI/UX, 웹 퍼블리싱 과정 |
| 2023.03 - 2024.02 | 주식회사 나으리 개발팀 사원                |
| 2024.03 - 2024.04 | 원티드 프리온보딩 프론트엔드 2024 Spring   |
| 2024.06 - 현재    | 주식회사 게더링 개발팀 사원                |

---

<br />
<br />

# 프로젝트

<br />

## 1. 루루봇 (2023.09 - 2024.02)

**링크:** [https://rooroo.kr/](https://rooroo.kr/)

**사용 기술:** `Next.js` `Typescript` `GitHub` `CSS3` `Bootstrap` `Context API` `Fabric.js` `TTS`

> 캔버스를 이용한 후원 꾸미기 및 스푼 방송 도움 프로그램

### 구현사항

- 유튜브 검색 API를 통한 검색 목록 출력 및 iframe으로 영상 표시
- 후원 기록 데이터를 API로 받아와 스티커 형태로 미리보기 제공
- 로컬 서버에 업로드한 이미지 미리보기 및 캔버스 표출
- JSON 형태의 Lottie 이미지 fetch 및 재생바를 통한 프레임 조절
- 캔버스 내 이미지 크롭 기능
- 사용자 모니터 크기 고려한 캔버스 줌인/줌아웃/이동 기능
- 캔버스 PNG 이미지로 고화질 다운로드

### 성과

- 기존 후원 꾸미기 시간 3-4시간에서 30-40분으로 단축

### 트러블슈팅

1. **Lottie 이미지 캔버스 표출 문제**
   - 문제
     - Lottie 이미지(JSON)를 재생, 정지 버튼으로 프레임을 조정하여 원하는 타이밍의 정지 이미지를 캔버스로 드래그앤드롭.
     - JSON 파일이 캔버스 용량문제로 그대로 업로드되지 못함.
     - 드래그앤드롭하는 순간 svg 파일로 업로드 처리하여 로컬 서버에 저장한 후, 캔버스에 표출
     - 하지만 정지했을 때의 이미지가 캔버스에 표출되어야 하는데, 그 전 정지된 이미지가 표출되는 등 의도대로 구현되지 않음.
     - 정지되었을 때의 Lottie 이미지 프레임(JSON)이 즉시 svg 파일화하여 캔버스에 업로드 되어야하는데, svg 파일 업로드 과정에서 즉각 반영이 안됨.
     - 재생, 정지 버튼만으로 원하는 프레임 선택이 어려워 사용성 문제O.
   - 해결
     - 재생/정지를 input type=range로 수정
     - Lottie 태그에 ref 및 스냅샷 버튼 추가
     - SVG 파일화 검증 로직 추가

<br />

## 2. 오락시설 중개 플랫폼, 픽플 (2023.07 - 2024.02)

**사용 기술:** `Next.js` `Typescript` `GitHub` `CSS3` `Bootstrap` `Context API` `FlutterFlow`

> 오락시설(PC방, 노래방) 중개 플랫폼

### 구현사항

- 상세페이지 구현 (리뷰, 게시글, 댓글, 답글 CRUD)
- 좋아요, 추천, 팔로우 기능
- 프로필 CRUD
- 이미지 업로드 API
- 관리자 페이지

### 트러블슈팅

1. **댓글/답글 구조화 문제**

   - 해결: 백엔드와 논의하여 API 엔드포인트 분리 및 컴포넌트 통합

2. **게시글 이미지 수정 에러**
   - 해결: 이미지 상태 분리 및 미리보기 로직 개선

<br />

## 3. 요양시설 중개 플랫폼, 나으리 (2023.03 - 2023.06)

**사용 기술:** `Next.js` `Typescript` `CSS` `HTML` `Javascript` `GitHub` `Bootstrap` `카카오지도 API` `네이버지도 API` `Context API`

> 공공데이터를 이용한 요양시설 정보 지도 검색 기능 제공 반응형 플랫폼

### 구현사항

- 카카오 맵과 네이버 지도 API를 사용한 지도 및 요양시설 목록 페이지
- 성능 개선을 위한 기술 스택 마이그레이션
  > HTML + jQuery → HTML + Vanila Javascript → Next.js 12 (pages directory) → Next.js 13 (app directory)
- 관리자 페이지

### 트러블슈팅

1. **페이지 로딩 속도 저하**

   - 해결: Next.js로 마이그레이션

2. **검색 기능 UX 개선**

   - 해결: 검색 관련 요소에 ID 부여 및 포커스 아웃 조건 정교화

3. **지도 마커 겹침 문제**
   - 해결: 줌 레벨별 마커 스타일 조정 및 커스텀 오버레이 적용

---

<br />
<br />

# 개인 토이 프로젝트

<br />

## 철BTI (2024.05) - 약 2일 소요

**링크:** [https://what-if-you-were-a-philosophy-student.vercel.app/](https://what-if-you-were-a-philosophy-student.vercel.app/)

**사용 기술:** `React` `Typescript` `styled-components` `google-analytics` `kakao-share-api` `Vercel`

> 21세기 대한민국 대학에서 철학과 진학시 가질 포지션 테스트
