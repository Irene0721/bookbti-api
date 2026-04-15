# 북BTI API 서버 (Vercel 배포용)

## 배포 방법

### 1. GitHub에 올리기
- GitHub.com 가입 후 새 repository 생성 (이름: bookbti-api)
- 이 폴더 파일들을 업로드

### 2. Vercel 연결
- vercel.com 가입 (GitHub 계정으로 로그인)
- "New Project" → bookbti-api repository 선택
- 자동 배포 완료

### 3. 환경변수 설정
- Vercel 대시보드 → 프로젝트 → Settings → Environment Variables
- 이름: ALADIN_TTB_KEY
- 값: ttbjongr211906001

### 4. 배포 URL 확인
- 배포 완료 후 URL: https://bookbti-api.vercel.app
- 테스트: https://bookbti-api.vercel.app/api/aladin?type=list&queryType=Bestseller&maxResults=5

## API 사용법

### 베스트셀러 목록
GET /api/aladin?type=list&queryType=Bestseller&maxResults=10

### 신간 목록
GET /api/aladin?type=list&queryType=ItemNewAll&maxResults=10

### 키워드 검색 (취향 기반 추천)
GET /api/aladin?type=search&query=힐링소설&maxResults=10

### 개별 책 조회 (표지/평점)
GET /api/aladin?type=lookup&isbn=9788936433598
